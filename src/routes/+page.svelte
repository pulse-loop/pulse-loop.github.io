<svelte:head>
	<title>pulse.loop</title>
	<meta name="description" content="An open source firmware for wearable pulse oximetry devices." />
</svelte:head>

<!-- Hero -->
<div class="section h-screen justify-center">
	<div class="flex flex-col items-center gap-5 p-4">
		<img
			class="sm:w-8/12"
			src="images/computer.png"
			alt="A computer with the pulse.loop app running."
		/>
		<h1 class="text-5xl font-semibold sm:text-7xl">pulse.loop</h1>
		<p class="w-2/3 text-center text-gray-600 sm:text-lg">
			An open source firmware for wearable pulse oximetry devices.
		</p>
	</div>
</div>

<!-- Goals -->
<div class="section loop-background bg-black">
	<div
		class="z-10 flex flex-col gap-4 self-start p-8 text-left text-pink-100 text-opacity-80 sm:p-12 md:p-16 lg:w-4/12 lg:p-24"
	>
		<h2
			class="bg-gradient-to-r from-pink-500 to-blue-500 bg-clip-text text-5xl font-semibold text-transparent"
		>
			Goals
		</h2>
		<p>
			The goal of this project is the development of a wrist-worn pulse oximeter. Detection of vital
			signs from the wrist is a challenging task, as the signal is weak and the sensor is prone to
			motion artifacts, but this positioning is ideal for comfortable continuous monitoring.
		</p>
		<p>
			Being a wearable device, it's important to have wireless access to recorded data. This is why
			we developed a companion app for iOS and macOS devices, along with two open source BLE
			modeling libraries.
		</p>
	</div>
	<img
		src="images/loop_mobile.jpg"
		alt="A render of an electronic bracelet."
		class="-mt-80 lg:hidden"
	/>
</div>

<!-- Hardware -->
<div class="section hardware-background">
	<div
		class="flex flex-col gap-4 self-end p-8 text-gray-700 sm:p-12 md:p-16 lg:w-7/12 lg:p-24 lg:text-right"
	>
		<h2 class="text-5xl font-semibold text-black">Hardware</h2>
		<p>
			The project is based on the AFE4404 analog front-end, which is an ultra-small integrated
			circuit for optical bio-sensing applications, such as monitoring heart rate and SpO2. It can
			control up to three LEDs using variable drive and offset currents. The current detected by the
			photodiode is then amplified by a transimpedance amplifier and converted into a digital signal
			by a 22-bit ADC, which allows for high resolution measurements.
		</p>
		<p>
			The AFE4404 is controlled by an ESP32-C3 microcontroller, which is a low-power, highly
			integrated Wi-Fi and Bluetooth LE SoC. It features a 32-bit RISC-V CPU with 4 MB of flash
			memory, allowing for development of complex applications. The ESP32-C3 is a great choice for
			this project because it's powerful enough to run advanced firmware among with the BLE stack,
			while retaining many power-efficient features. Being compatible with LLVM-based toolchains,
			the RISC-V core can be programmed in a variety of languages, including Rust.
		</p>
	</div>
</div>

<!-- Firmware -->
<div class="section firmware-background bg-black">
	<div
		class="z-10 flex flex-col gap-4 self-start p-8 text-gray-400 sm:p-12 md:p-16 lg:w-6/12 lg:p-24"
	>
		<h2
			class="bg-gradient-to-r from-lime-200 to-blue-500 bg-clip-text text-5xl font-semibold text-transparent"
		>
			Firmware
		</h2>
		<p>
			The firmware runs on top of the ESP-IDF framework, and plays a crucial role in ensuring
			accurate and reliable measurements. The automatic gain control adjusts the current of three
			LEDs to account for variations in reflected light intensity, keeping the signal within the
			dynamic range of the ADC. The wrist detection algorithm helps to filter out any meaningless
			readings, and the digital filters extract the DC and AC components of the signal, which are
			then used to calculate the SpO2 and heart rate values.
		</p>
		<p>
			The Rust programming language was chosen for the development of the firmware, as it provides
			many safety guarantees that are crucial for multi-threaded applications. Support for the
			AFE4404 analog front-end is provided by a custom driver, based on the <code>embedded-hal</code
			>
			traits. This way, the driver can be used on any microcontroller that implements it. The Bluedroid
			Bluetooth LE stack was wrapped inside a safe Rust library, and it's making its way to become the
			official implementation of BLE in <code>esp-idf-hal</code>.
		</p>
	</div>
</div>

<!-- Software -->
<div class="section software-background z-10">
	<div class="flex flex-row justify-between">
		<div />
		<div
			class="flex flex-col gap-4 p-8 text-gray-700 sm:p-12 md:p-16 lg:w-5/12 lg:p-24 lg:text-right"
		>
			<h2 class="text-5xl font-semibold text-black">Software</h2>
			<p>
				The companion app developed for the project is developed in SwiftUI, a declarative UI
				framework, and it's available for iOS and macOS devices. The application connects to the
				pulse oximeter via Bluetooth Low Energy, enabling the real-time data monitoring and
				visualization. CharacteristicKit is a library which uses metaprogramming concepts to allow
				for an easy modelling of Bluetooth LE peripherals, and it's used as an high level
				abstraction layer over Core Bluetooth.
			</p>
			<p>
				This software is not meant to be used by the end user, as it allows the set-up of many
				internal parameters. However, it can be used to test the device and to collect data for
				further analysis, and it's easily reducible to a simple monitoring app, while retaining to
				internally change the parameters, with no intervention from the user.
			</p>
		</div>
	</div>
</div>

<!-- Results -->
<div class="section results-background bg-gray-50">
	<div class="flex flex-row justify-between">
		<div class="flex flex-col gap-4 p-8 text-left text-gray-700 sm:p-12 md:p-16 lg:w-5/12 lg:p-24">
			<h2 class="text-5xl font-semibold text-black">Results</h2>
			<p>
				In conclusion, the pulse oximeter was calibrated against a commercial device and the
				resulting data was processed with a MATLAB script. A regression model was obtained, which
				can be used to calculate the SpO2 from our device's measurements. The results show that the
				pulse oximeter is able to detect the heart rate and SpO2 with reasonable accuracy,
				considering the sensor location, which inherently presents certain limitations. Despite
				this, the project's outcome indicate the feasibility of utilizing a wrist-worn pulse
				oximeter for non-invasive monitoring.
			</p>
			<p>
				However, there is still room for improvement. Future iterations could benefit from a
				calibration process conducted in a laboratory setting and further statistical analysis to
				enhance the accuracy and reliability of the measurements.
			</p>
		</div>
	</div>
</div>

<!-- Resources -->
<div class="section">
	<h2 class="pl-8 pt-20 text-5xl font-semibold sm:pl-12 md:pl-16 lg:pl-24">Resources</h2>
	<div
		class="hidden-scrollbar pb-8 flex flex-row flex-nowrap gap-6 overflow-x-auto px-8 sm:px-12 md:px-16 lg:px-24"
	>
		<div class="res-card">
			<img src="images/hr3.png" alt="Mikroe Heart Rate 3 Click" />
			<span>
				<h3>Heart rate 3</h3>
				<h5>Mikroe</h5>
				<a href="https://www.mikroe.com/heart-rate-3-click" target="_blank">Buy from Mikroe</a>
			</span>
		</div>

		<div class="res-card">
			<img src="images/esp32c3.png" alt="ESP32-C3 Development Board" />
			<span>
				<h3>ESP32-C3 DevKitM-1</h3>
				<h5>Espressif</h5>
				<a
					href="https://www.mouser.it/ProductDetail/Espressif-Systems/ESP32-C3-DevKitM-1?qs=pUKx8fyJudB1sOWbbEnGFw%3D%3D"
					target="_blank">Buy from Mouser</a
				>
			</span>
		</div>

		<div class="res-card">
			<img src="logos/macos_app.png" alt="pulse.loop app icon" class="mt-12 scale-125" />
			<span>
				<h3>pulse.loop client</h3>
				<h5>Source code</h5>
				<a href="https://github.com/pulse-loop/pulse.loop" target="_blank">See on GitHub</a>
			</span>
		</div>

		<div class="res-card">
			<img src="logos/CharacteristicKit.png" alt="CharacteristicKit icon" class="mt-10 scale-125" />
			<span>
				<h3>CharacteristicKit</h3>
				<h5>Swift Package</h5>
				<a href="https://github.com/persello/CharacteristicKit" target="_blank">See on GitHub</a>
			</span>
		</div>

		<div class="res-card">
			<img src="logos/pl.png" alt="pulse.loop icon" class="mt-20" />
			<span>
				<h3>Firmware</h3>
				<h5>Source code</h5>
				<a href="https://github.com/pulse-loop/firmware" target="_blank">See on GitHub</a>
			</span>
		</div>

		<div class="res-card">
			<img src="logos/crates.png" alt="crates.io Logo" class="mt-12 scale-125" />
			<span>
				<h3>Bluedroid</h3>
				<h5>Rust crate</h5>
				<a href="https://crates.io/crates/bluedroid" target="_blank">See on crates.io</a>
			</span>
		</div>

		<div class="res-card">
			<img src="logos/crates.png" alt="crates.io Logo" class="mt-12 scale-125" />
			<span>
				<h3>AFE4404</h3>
				<h5>Rust crate</h5>
				<a href="https://crates.io/crates/afe4404" target="_blank">See on crates.io</a>
			</span>
		</div>
	</div>
</div>

<!-- Footer -->
<div class="footer text-gray-500">
	<div class="flex flex-col">
		<h4 class="font-bold text-black">pulse.loop</h4>
		<p>Open Source Pulse-Oximetry Firmware</p>
		<p><a href="https://uniud.it">Università degli Studi di Udine</a></p>
	</div>

	<div class="lg:mx-auto flex w-min flex-col">
		<div class="my-1 flex flex-row justify-between">
			<h4 class="font-bold text-black">Fabio Cragnolini</h4>
			<span class="flex flex-row gap-2">
				<a href="https://github.com/FabioCragnolini" target="_blank"
					><img src="logos/github.svg" class="h-5 w-5" alt="GitHub Logo" /></a
				>
				<a href="https://linkedin.com/in/fabiocragnolini" target="_blank"
					><img src="logos/linkedin.svg" class="h-5 w-5" alt="LinkedIn Logo" /></a
				>
			</span>
		</div>
		<code><a href="mailto:fbcragnolini@gmail.com">fbcragnolini@gmail.com</a></code>
	</div>

	<div class="lg:mx-auto flex w-min flex-col">
		<div class="my-1 flex flex-row justify-between">
			<h4 class="font-bold text-black">Riccardo Persello</h4>
			<span class="flex flex-row gap-2">
				<a href="https://github.com/persello" target="_blank"
					><img src="logos/github.svg" class="h-5 w-5" alt="GitHub Logo" /></a
				>
				<a href="https://linkedin.com/in/riccardo-persello" target="_blank"
					><img src="logos/linkedin.svg" class="h-5 w-5" alt="LinkedIn Logo" /></a
				>
			</span>
		</div>
		<code><a href="mailto:riccardo.persello@icloud.com">riccardo.persello@icloud.com</a></code>
	</div>
</div>

<style lang="scss">
	.res-card {
		@apply z-10 my-4 flex w-64 flex-none flex-col justify-between overflow-clip rounded-2xl bg-gray-50 p-8;

		img {
			@apply mb-4 object-contain p-8;
		}

		h3 {
			@apply mt-2 text-2xl font-bold text-black;
		}

		h5 {
			@apply font-semibold uppercase tracking-wider text-gray-400;
		}

		span {
			@apply flex flex-col;

			a {
				@apply -m-8 mt-4 self-stretch bg-blue-100 p-4 text-center font-semibold text-blue-500 transition-all hover:bg-blue-600 hover:text-white;
			}
		}
	}

	.hidden-scrollbar::-webkit-scrollbar {
		display: none;
	}

	.hidden-scrollbar {
		-ms-overflow-style: none;
		scrollbar-width: none;
	}

	.section {
		@apply flex flex-col gap-4 leading-8 sm:text-lg;
		min-height: 40rem;
	}

	.footer {
		@apply grid lg:grid-cols-3 bg-gray-50 px-8 sm:px-12 md:px-16 lg:px-24 pb-32 pt-12 gap-12;

		h4 {
			@apply mb-2;
		}
	}

	.loop-background {
		@media screen and (min-width: 1024px) {
			background-image: url('../../../images/loop.jpg');
			background-size: cover;
			background-position: center;
		}
	}

	.hardware-background {
		@media screen and (min-width: 1024px) {
			background-image: url('../../../images/hardware.jpg');
			background-size: cover;
			background-position: bottom;
		}
	}

	.firmware-background {
		@media screen and (min-width: 1024px) {
			background-image: url('../../../images/code.jpg');
			background-size: cover;
			background-position: bottom;
		}
	}

	.software-background {
		@media screen and (min-width: 1024px) {
			background-image: url('../../../images/Xcode.png');
			background-size: 60%;
			background-position: -30%;
			background-repeat: no-repeat;
		}
	}

	.results-background {
		@media screen and (min-width: 1024px) {
			background-image: url('../../../images/MATLAB.png');
			background-size: 60%;
			background-position: 130%;
			background-repeat: no-repeat;
		}
	}
</style>
