Sensors
######

Overview
********

This sample is to read the data from the BME680 and LIS3MDL. The nRF52833 reads the data through I2C0 interface. You can see the devicetree in boards/arm/tautek/tautek.dts

<br>

&i2c0 {  <br>                            
	compatible = "nordic,nrf-twi";  <br>
	status = "okay";<br>
	pinctrl-0 = <&i2c0_default>;<br>
	pinctrl-1 = <&i2c0_sleep>;<br>
	pinctrl-names = "default", "sleep";<br>
<br>
	bme680@76 {<br>
		compatible = "bosch,bme680";<br>
		reg = <0x76>;<br>
	};<br>
	lis3mdl@1c {<br>
		compatible = "st,lis3mdl-magn";<br>
		reg = <0x1c>;<br>
	};<br>

When you build the project, you can select the prj_logs.conf to print the log on the RTT Viewer. To print the log on the serial interface(Tx, Rx), you can use prj.conf.