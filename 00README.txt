GeoNEX ONLINE DATAPOOL
-----------------------------
Datapool readme file, last updated 2020-07-24.


DATA STATUS & RELEASE CADENCE 
-----------------------------
All product are considered provisional and subject to change. Products are intended to facilitate data exploration 
and process studies that do not require rigorous validation. These data may be partially validated and improvements 
are continuing; quality may not be optimal since validation and quality assurance are ongoing. See disclaimer below.

GeoNEX gridded products are currently be updated on a semiannual or best effort basis. The release cadence is expected
to increase with future product and process improvements. All updates will be announced through the GeoNEX mailing 
list at lists.nasa.gov.    


DATA DIRECTORIES
-----------------------------

* GOES16/GEONEX-L1G/
             Top-of-Atmosphere (TOA) reflectance GOES-16 ABI. This product includes the Bidirectional Reflectance 
             Factor (BRF) for Bands 1-6 and Brightness Temperature for Bands 7-16 at the top of the atmosphere 
             measured by the satellite sensor.  BRF is defined as the ratio of the radiance reflected from the 
             target surface (e.g., top of atmosphere) in a particular direction to the expected radiance reflected 
             from a perfectly white Lambertian surface in the same direction under the same conditions of illumination 
             and reflection.  The phrase "bidirectional" emphasizes that the variable is a function of both solar incident 
             and satellite-viewing angles. Brightness temperature is the temperature of a blackbody that would emit the 
             same amount of radiation as the targeted body in a specified spectral band. It is different from the true 
             surface temperature because (1) the surface is not a perfect blackbody; and (2) it is influenced by atmospheric
             conditions. For more information on the steps used to create this product see https://www.nasa.gov/geonex.

* GOES16/GEONEX-L2/
            GOES16 surface reflectance (Surface BRF) estimated through the process of atmospheric correction for Bands 1-6.SR is calculated 
            by removing the atmospheric influence (absorption and scattering by molecules and aerosols) from the TOA reflectance. 
            The data are also filtered for unfavorable conditions (e.g., clouds and shadows) under which the retrieval of SR is not 
            feasible or reliable.  Intermediate products include cloud masks, atmospheric aerosol optical thickness (AOT), surface 
            BRDF parameters, and so on.

            The current surface reflectance dataset is produced with an early version of MAIAC. The accuracy of cloud 
            detection and aerosol retrievals is not yet sufficient for science publications. We are still working on 
            issues with the BRDF model fit and atmospheric correction. The next improved version of MAIAC is in a stage 
            of completion, and the updated results of processing will be available the in near future.

* GOES16/NOAA-L1B/
            GeoNEX GOES16 INPUTS


* GOES17/GEONEX-L1G/
            Top-of-Atmosphere (TOA) reflectance GOES-17 ABI. Refer to GOES16/GEONEX-L1G/ directory write-up, or the website, 
            for more information.


* GOES17/GEONEX-L2/
            GOES17 surface reflectance (Surface BRF) estimates. Refer to GOES16/GEONEX-L2/ directory write-up, or the website, 
            for more information.

* GOES17/NOAA-L1B/
            GeoNEX GOES17 INPUTS


* HIMAWARI8/GEONEX-L1G/ 
            Top-of-Atmosphere (TOA) reflectance HIMAWARI8. Refer to GOES16/GEONEX-L1G/ directory write-up, or the website, for more information.


* HIMAWARI8/GEONEX-L2/ 
            HIMAWARI8 surface reflectance (Surface BRF) estimates. Refer to GOES16/GEONEX-L2/ directory write-up, or the website, 
            for more information.


* HIMAWARI8/JMA-L1/
            GeoNEX HIMAWARI8 INPUTS. See https://www.data.jma.go.jp/mscweb/en/himawari89/space_segment/spsg_sample.html (link valid 2019) 
            for more information.

* GK2A/AMI/
            GeoNEX GEO-KOMPSAT-2A INPUTS. See https://nmsc.kma.go.kr/enhome/html/base/cmm/selectPage.do?page=satellite.gk2a.intro (link vaid 2020)
            The data set is available to internal hecc users; to be exported soon. 


* MOTA/MCD12Q1.006/
            This is a convenience data set which is a GeoNEX tiled MCD12Q1 product. MCD12Q1 is a Terra and Aqua combined Moderate Resolution 
            Imaging Spectroradiometer (MODIS) Land Cover Type (MCD12Q1) data product which provides global land cover types. 


* META/
            This directory contains some convenience files and information on spatial information, rudimentary indexing, etc...

* NEX-GDM/
            This directory contains the auxiliary data set NEX-Gridded Daily Meteorology (NEX-GDM) land surface climate data. The
            data set is available from 1979 to forward, over the conterminous US and is updated on a best effort basis. NEX-GDM 
            is a 1-km daily climate data, including precipitation, minimum temperature, maximum temperature, dew point temperature, 
            wind speed, and solar radiation. 


All data is available in the internal datapools (/nex/datapool/) for NEX/NAS users. The data exported on the dataportal is often
significantly behind of internal sources, the export or refresh rate will improve with time.
            

FILE NAMING CONVENTIONS FOR L1G DATA 
-----------------------------
For all GeoNEX products, the following naming convention is used:

<Satellite/Sensor Code><ProductID>_<YYYYMMDD>_<HHMM>_GLBG_h<hid>v<vid>_<version>.hdf

<Satellite/Sensor Code>: HM08_AHI for Himawari 8 AHI, and GO16_ABI or GO17_ABI for GOES

<Product ID>: A two-digit number assigned to each GeoNEX product. Currently, only the Product ID of "05" is 
              available, indicating "Top-of-Atmosphere Reflectance"

<YYYYMMDD>: Year-Month-Day, e.g., 20180501

<HHMM>: Hour-Minute (UTC time), e.g., 2030

<hid>, <vid>: Horizontal or Vertical Tile ID (0-19)

<version>: Product version code. It is currently "002"

Note, the input and convenience products may differ from the above naming convention.


REFERENCES
-----------------------------
Wang, W., Li, S., Hashimoto, H., Takenaka, H., Higuchi, A., Kalluri, S., and Nemani, R.R., (2019a) An Introduction to the Geostationary-NASA 
(GeoNEX) Products: 1. Top-of-Atmosphere Reflectance and Brightness Temperature. Remote Sensing (to be submitted).


COMMUNITY AND SUPPORT
-----------------------------
For specific support questions and issues with the data products email support@nas.nasa.gov 
and include "GeoNEX" in the subject line. You may wish to register with the GeoNEX mailing list 
geonex@lists.nasa.gov, see https://lists.nasa.gov/mailman/listinfo/geonex/, where community 
support and data status announcements will be provided. 


DISCLAIMER
-----------------------------
The data are considered provisional and subject to change. The data are provided as is without any warranty of any 
kind, either express or implied, arising by law or otherwise, including but not limited to warranties of completeness, 
non-infringement, accuracy, merchantability, or fitness for a particular purpose. The user assumes all risk associated 
with the use of, or inability to use, the data.

