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
	<div class="flex w-3/12 flex-col gap-4 self-start text-left text-lg leading-8 text-gray-300">
		<h2 class="text-5xl font-semibold text-white">Goals</h2>
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
	<div class="flex w-5/12 flex-col gap-4 self-end text-right text-lg leading-8 text-gray-700">
		<h2 class="text-5xl font-semibold text-black">Hardware</h2>
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

<!-- Firmware -->
<div class="section firmware-background">
	<div class="flex w-5/12 flex-col gap-4 self-start text-left text-lg leading-8 text-gray-300">
		<h2 class="text-5xl font-semibold text-white">Firmware</h2>
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

<!-- Software -->
<div class="section">
	<div class="flex flex-row justify-between">
		<img
			src="Xcode.png"
			class="w-5/12 object-contain"
			alt="An Xcode screenshot showing the development of the companion software."
		/>
		<div class="flex w-5/12 flex-col gap-4 text-right text-lg leading-8 text-gray-700">
			<h2 class="text-5xl font-semibold text-black">Software</h2>
			<p>
				The goal of this project is the development of a wrist-worn pulse oximeter. Detection of
				vital signs from the wrist is a challenging task, as the signal is weak and the sensor is
				prone to motion artifacts, but this positioning is ideal for comfortable continuous
				monitoring.
			</p>
			<p>
				Being a wearable device, it's important to have wireless access to recorded data. This is
				why we developed a companion app for iOS and macOS devices, along with two open source BLE
				modeling libraries.
			</p>
		</div>
	</div>
</div>

<!-- Results -->
<div class="section bg-gray-100">
	<div class="flex flex-row justify-between">
		<div class="flex w-5/12 flex-col gap-4 text-left text-lg leading-8 text-gray-700">
			<h2 class="text-5xl font-semibold text-black">Results</h2>
			<p>
				The goal of this project is the development of a wrist-worn pulse oximeter. Detection of
				vital signs from the wrist is a challenging task, as the signal is weak and the sensor is
				prone to motion artifacts, but this positioning is ideal for comfortable continuous
				monitoring.
			</p>
			<p>
				Being a wearable device, it's important to have wireless access to recorded data. This is
				why we developed a companion app for iOS and macOS devices, along with two open source BLE
				modeling libraries.
			</p>
		</div>
		<!-- TODO: New screenshot. -->
		<img
			src="MATLAB.png"
			class="w-5/12 object-contain"
			alt="A MATLAB screenshot showing correlation data for oximetry measurements."
		/>
	</div>
</div>

<!-- Resources -->
<div class="section">
	<h2 class="text-5xl font-semibold">Resources</h2>
	<!-- TODO: Better classes, move padding to blocks. -->
</div>

<!-- Footer -->

<style lang="scss">
	.section {
		@apply flex flex-col gap-4 p-24;
		min-height: 40rem;
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
</style>
