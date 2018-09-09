## Content

* A library of (semi-)empirical SED templates to reconcile the dust emission of type-1 AGNs with a wide range of luminosity (<a href="https://www.codecogs.com/eqnedit.php?latex=L_{\rm&space;bol}\sim10^8-10^{14}L_\odot" target="_blank"><img src="https://latex.codecogs.com/gif.latex?L_{\rm&space;bol}\sim10^8-10^{14}L_\odot" title="L_{\rm bol}\sim10^8-10^{14}L_\odot" /></a>) and redshift (<a href="https://www.codecogs.com/eqnedit.php?latex=z\sim0-6" target="_blank"><img src="https://latex.codecogs.com/gif.latex?z\sim0-6" title="z\sim0-6" /></a>), as gradually developed .

Normal  AGNs    |   Warm-dust-Deficient AGNs   | Hot-Dust-Deficient AGNs 
:--------------:|:----------------------------:|:------------------------:
![]()   | ![]() | ![]()

* AGN host galaxy templates that has been used for low-zworks at z<4 and z\sim4-6

Host galaxy FIR templates                                                     |   Host galaxy stellar emission template
:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:
![](https://github.com/karlan/AGN_templates/raw/master/plots/galaxy_fir.png)  |  ![](https://github.com/karlan/AGN_templates/raw/master/plots/stellar_template.png)
Comparison of Haro 11 template (red line) and the normal star-forming galaxy templates with log LIR = 9.75 ~ 11.50 in Rieke et al. (2009) (blue lines). All the templates are normalized to have the same LIR,template. |Comparisons of different stellar templates. We derive an empirical template by replacing a Bruzual & Charlot (2003) 7 Gyr SSP SED template with the mid-IR (6–20 μm) stellar template and a power-law SED (λ >20 μm). We plot the individual Spitzer/IRS spectra used to derived the mid-IR template as grey lines. The original Bruzual & Charlot (2003) and the elliptical galaxy templates with age 2, 5 and 13 Gyr from the SWIRE library (Polletta et al. 2007) are also presented.


## Directory information

       AGN_intrinsic/
            AGN_torus_faceon.temp.full.txt             -- intrinsic templates for normal, warm-dust-deficient and hot-dust-deficient AGNs
            AGN_polar_emission.temp.full.txt           -- template for the polar dust emission as trained for low-z Seyfert-1 nuclei
             
    
       AGN_reddend_lib/  
            norm/  
                  norm-[id].dat    -- reddened templates for normal AGNs, tau_{pol, V}= 0 - 5
            hdd/  
                  hdd-[id].dat     -- reddened templates for hot-dust-deficient AGNs, tau_{pol, V}= 0 - 5
            wdd/
                  wdd-[id].dat     -- reddened tempaltes for warm-dust-deficient AGNs, tau_{pol, V}= 0 - 5
            hdo/  
                  hdo-[id].dat     -- hot dust-obscured templates for normal AGNs, tau_{pol, V}= 0 - 5

            obsagn_temp.norm.index.lis   -- ID, tau_{pol, V} and f_{pol, 10\mum} information for templates in norm/
            obsagn_temp.hdd.index.lis    --  **** in hdd/           
	    obsagn_temp.wdd.index.lis    --  **** in wdd/
            obsagn_temp.hdo.index.lis    --  **** in hdo/
             
    
       host_galaxy/  
            normal_SFGs/  
                  rieke-F[loglum]_temp.txt   -- Rieke + 2009 SFG tempaltes, loglum = alog10(L_{IR}/L_sun)
            lometal_starburst/  
                  Haro11.temp.full.txt       -- Haro 11 far-IR template
            old_stars.temp.full.txt          -- template for old stellar population with mid-IR dust features
    
       plots/        -- plots for these templates
    
       README.md

## Usage Guidelines

## Cautionary Notes

## Citations
 
