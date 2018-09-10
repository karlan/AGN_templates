## Content

* A library of (semi-)empirical SED templates to reconcile the dust emission of type-1 AGNs with a wide range of luminosity (<a href="https://www.codecogs.com/eqnedit.php?latex=L_{\rm&space;bol}\sim10^8-10^{14}L_\odot" target="_blank"><img src="https://latex.codecogs.com/gif.latex?L_{\rm&space;bol}\sim10^8-10^{14}L_\odot" title="L_{\rm bol}\sim10^8-10^{14}L_\odot" /></a>) and redshift (<a href="https://www.codecogs.com/eqnedit.php?latex=z\sim0-6" target="_blank"><img src="https://latex.codecogs.com/gif.latex?z\sim0-6" title="z\sim0-6" /></a>), as developed in 
  * [Lyu, Rieke & Shi 2017](http://adsabs.harvard.edu/abs/2017ApJ...835..257L) (variations of AGN intrinsic IR emission; normal bright quasars, dust-free/poor quasars)
  * [Lyu & Rieke 2017](http://adsabs.harvard.edu/abs/2017ApJ...841...76L) (the correct SED shape of AGN intrinsic far-IR emission)
  * [Lyu & Rieke 2018]()(the effect of polar dust component; low-z Seyfert-1 nuclei, extremely red quasars, AGNs with warm-excess emission, hot dust-obscured galaxies)

* Empirical IR templates for AGN host galaxies that have been suggested to decomposte the quasars SEDs at z=5-7 ([Lyu, Rieke & Alberts 2016](http://adsabs.harvard.edu/abs/2016ApJ...816...85L)) and those at z<4 (see [Lyu & Rieke 2017](http://adsabs.harvard.edu/abs/2017ApJ...841...76L))

Three flavors of type-1 AGN intrinsic IR emision|
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
The AGN templates here have been constructed in a "minimalist" style: we wish
to build SED models with the numbers of free parameters as small as possible.
Based on real observations, we derived three intrinsic templates to describe
the SEDs of accretion disk + torus emission as seen from a face-on viewing
angle (aka, Type-1), tested their robustness with independent calibrations
avaliable for PG quasars, and demonstrated such variations could be common at
different redshifts and AGN luminosities. Then we introduced a very simple
polar dust model that could obscure the intrinsic AGN templates, and showed
that it worked reasonablly well to reproduce the polar dust emission strength
observed in nearby Seyfert-1 nuclei and to reconcile the SED behaviors of
various type-1 AGN populations. These templates can be generally applied in
e.g.,  SED decompositions of galaxies with possible AGN contribution or
quasars, IR AGN Selections and the search for pecuilar objects, etc.
    
However, although these templates are empirically constructed and tested
against various observations, they should be applied correctly to get
scientifically reasonable results (you should never trust any fitting results
just because the chi-square was very small).
    

## Cautionary Notes
 * All the AGN and galaxy templates have been interpolated on the same wavelength grids with relatively high spectral resolutions. However, these templates are constructed to reproduce the broad-band SEDs only;
 * The AGN templates are designed to be used only for type-1 objects (aka. AGNs with broad emission lines). We currently do not have a good idea on the IR emission behaviors of the "edge-on" torus, given the possible contaminations of polar dust and host galaxy dust.
