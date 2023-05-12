<!-- Hero -->
<div class="section h-screen justify-center">
	<div class="flex flex-col items-center gap-5">
		<img class="w-8/12" src="computer.png" alt="A computer with the pulse.loop app running." />
		<h1 class="text-7xl font-semibold">pulse.loop</h1>
		<p class="text-lg text-gray-600">
			An open source firmware for wearable pulse oximetry devices.
		</p>
	</div>
</div>

<!-- Goals -->
<div class="section loop-background">
	<div class="flex w-4/12 flex-col gap-4 self-start text-left text-lg leading-8 text-pink-100">
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
</div>

<!-- Hardware -->
<div class="section hardware-background">
	<div class="flex w-7/12 flex-col gap-4 self-end text-right text-lg leading-8 text-gray-700">
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
<div class="section firmware-background">
	<div class="flex w-6/12 flex-col gap-4 self-start text-lg leading-8 text-gray-400">
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
<div class="section software-background">
	<div class="flex flex-row justify-between">
		<div />
		<div class="flex w-5/12 flex-col gap-4 text-right text-lg leading-8 text-gray-700">
			<h2 class="text-5xl font-semibold text-black">Software</h2>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae porro labore sint iste
				iure impedit voluptatum veniam accusantium architecto voluptate officiis, officia minima,
				incidunt qui atque cupiditate neque fugiat doloribus.
			</p>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste ea, ad a recusandae, at, et
				illo tempore nulla sint aperiam placeat asperiores earum laudantium. Magnam corporis dolorem
				ab asperiores esse.
			</p>
		</div>
	</div>
</div>

<!-- Results -->
<div class="section bg-gray-50 results-background">
	<div class="flex flex-row justify-between">
		<div class="flex w-5/12 flex-col gap-4 text-left text-lg leading-8 text-gray-700">
			<h2 class="text-5xl font-semibold text-black">Results</h2>
			<p>
				Lorem, ipsum dolor sit amet consectetur adipisicing elit. Numquam expedita veritatis eum
				quasi voluptate recusandae doloribus voluptatem. Reiciendis fugiat eius eum facilis harum
				mollitia, delectus eligendi hic! Tenetur, quasi odit!
			</p>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum dolorem earum architecto,
				nemo ratione non est minus quia impedit sint aliquid blanditiis eum assumenda nisi ipsa
				illum, facere optio ullam.
			</p>
		</div>
	</div>
</div>

<!-- Resources -->
<div class="section">
	<h2 class="text-5xl font-semibold">Resources</h2>
	<div class="flex flex-row overflow-x-auto">
		<div class="res-card">
			<img src="hr3.png" />
			<h3>Heart rate 3</h3>
			<h5>Mikroe</h5>
		</div>

		<div class="res-card">
			<img src="hr3.png" />
			<h3>Heart rate 3</h3>
			<h5>Mikroe</h5>
		</div>

		<div class="res-card">
			<img src="hr3.png" />
			<h3>Heart rate 3</h3>
			<h5>Mikroe</h5>
		</div>

		<div class="res-card">
			<img src="hr3.png" />
			<h3>Heart rate 3</h3>
			<h5>Mikroe</h5>
		</div>

		<div class="res-card">
			<img src="hr3.png" />
			<h3>Heart rate 3</h3>
			<h5>Mikroe</h5>
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

	<div class="mx-auto flex w-min flex-col">
		<div class="my-1 flex flex-row justify-between">
			<h4 class="font-bold text-black">Fabio Cragnolini</h4>
			<span class="flex flex-row gap-2">
				<a href=""><img src="github.svg" class="h-5 w-5" alt="GitHub Logo" /></a>
				<a href=""><img src="linkedin.svg" class="h-5 w-5" alt="LinkedIn Logo" /></a>
			</span>
		</div>
		<code><a href="mailto:fbcragnolini@gmail.com">fbcragnolini@gmail.com</a></code>
	</div>

	<div class="mx-auto flex w-min flex-col">
		<div class="my-1 flex flex-row justify-between">
			<h4 class="font-bold text-black">Riccardo Persello</h4>
			<span class="flex flex-row gap-2">
				<a href=""><img src="github.svg" class="h-5 w-5" alt="GitHub Logo" /></a>
				<a href=""><img src="linkedin.svg" class="h-5 w-5" alt="LinkedIn Logo" /></a>
			</span>
		</div>
		<code><a href="mailto:riccardo.persello@icloud.com">riccardo.persello@icloud.com</a></code>
	</div>
</div>

<style lang="scss">
	.res-card {
		@apply m-6 flex w-96 flex-col rounded-lg bg-gray-50 p-8 shadow-md transition-shadow duration-300 hover:shadow-lg;

		img {
			@apply mb-4 max-h-48 object-contain drop-shadow-lg;
		}

		h3 {
			@apply text-2xl font-semibold text-black;
		}

		h5 {
			@apply text-gray-500;
		}
	}

	.section {
		@apply flex flex-col gap-4 p-24 overflow-clip;
		min-height: 40rem;
	}

	.footer {
		@apply grid grid-cols-3 bg-gray-50 px-36 pb-32 pt-12;

		h4 {
			@apply mb-2;
		}
	}

	.loop-background {
		background-image: url('../../../loop.jpg');
		background-size: cover;
		background-position: center;
	}

	.hardware-background {
		background-image: url('../../../hardware.jpg');
		background-size: cover;
		background-position: bottom;
	}

	.firmware-background {
		background-image: url('../../../code.jpg');
		background-size: cover;
		background-position: bottom;
	}

	.software-background {
		background-image: url('../../../Xcode.png');
		background-size: 60%;
		background-position: -30%;
		background-repeat: no-repeat;
	}

	.results-background {
		background-image: url('../../../MATLAB.png');
		background-size: 60%;
		background-position: 130%;
		background-repeat: no-repeat;
	}
</style>
