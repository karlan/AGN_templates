## Content

* A library of (semi-)empirical SED templates to reconcile the dust emission of type-1 AGNs with a wide range of luminosity (<a href="https://www.codecogs.com/eqnedit.php?latex=L_{\rm&space;bol}\sim10^8-10^{14}L_\odot" target="_blank"><img src="https://latex.codecogs.com/gif.latex?L_{\rm&space;bol}\sim10^8-10^{14}L_\odot" title="L_{\rm bol}\sim10^8-10^{14}L_\odot" /></a>) and redshift (<a href="https://www.codecogs.com/eqnedit.php?latex=z\sim0-6" target="_blank"><img src="https://latex.codecogs.com/gif.latex?z\sim0-6" title="z\sim0-6" /></a>), as developed in 
  * [Lyu, Rieke & Shi 2017](http://adsabs.harvard.edu/abs/2017ApJ...835..257L) (variations of AGN intrinsic IR emission; normal bright quasars, dust-free (or poor) quasars)
  * [Lyu & Rieke 2017](http://adsabs.harvard.edu/abs/2017ApJ...841...76L) (the correct SED shape of AGN intrinsic far-IR emission)
  * [Lyu & Rieke 2018]()(the effect of polar dust component; low-z Seyfert-1 nuclei, extremely red quasars, AGNs with warm-excess emission, hot dust-obscured galaxies)

* Empirical IR templates for AGN host galaxies that has been suggested to decomposte the quasars SEDs at z=5-7 ([Lyu, Rieke & Alberts 2016](http://adsabs.harvard.edu/abs/2016ApJ...816...85L)) and those at z<4 (see [Lyu & Rieke 2017](http://adsabs.harvard.edu/abs/2017ApJ...841...76L))

Three flavors of AGN intrinsic IR emision|
:--------------------------------------------:|
![](https://github.com/karlan/AGN_templates/raw/master/plots/AGN_intrinsic_template.png)|
Comparison of the hot-dust-deficient (HDD) AGN template (left panel, red solid line) and the warm-dust-deficient (WDD) template (right panel, green solid line) to the normal Elvis et al. (1994) AGN template (far-IR corrected by Xu et al. 2015; blue solid line).|
see [Lyu, Rieke & Shi 2017](http://adsabs.harvard.edu/abs/2017ApJ...835..257L) for details|


<table>
<tr>
<td colspan="3" align="center"> Usage Demonstrations of the Reddened AGN Templates </td>   
</tr>
<tr>
<td> <img src="https://github.com/karlan/AGN_templates/raw/master/plots/NGC3783.png" /> </td> 
<td> <img src="https://github.com/karlan/AGN_templates/raw/master/plots/ERQ.png" /> </td> 
<td> <img src="https://github.com/karlan/AGN_templates/raw/master/plots/HotDOG.png" /> </td> 
</tr>
<tr>
  <td> NGC 3783: a Seyfert-1 nuclei with confirmed mid-IR polar dust emission </td>
  <td>  Extremely Red Quasars  </td>
  <td> Hot Dust-Obscured Galaxies </td>
  </tr>
<td colspan="3" align="center"> see [Lyu & Rieke 2018]() for details  </td>
</table>






Host galaxy FIR templates                                                     |   Host galaxy stellar emission template
:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:
![](https://github.com/karlan/AGN_templates/raw/master/plots/galaxy_fir.png)  |  ![](https://github.com/karlan/AGN_templates/raw/master/plots/stellar_template.png)
Comparison of Haro 11 template (red line) and the normal SFG templates in Rieke et al. (2009) (blue lines). | Comparisons of different stellar templates. The final empirical stellar template is shown as a green line.
| see [Lyu, Rieke & Alberts 2016](http://adsabs.harvard.edu/abs/2016ApJ...816...85L) for details |  see [Lyu & Rieke 2018]() for details 

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
                  Haro11.temp.full.txt       -- Haro 11 far-IR template, suggested to be used for quasar hosts at z>5
            old_stars.temp.full.txt          -- template for old stellar population with mid-IR dust features
    
       plots/        -- plots for these templates
    
       README.md

## Usage Guidelines

## Cautionary Notes

## Citations
 
