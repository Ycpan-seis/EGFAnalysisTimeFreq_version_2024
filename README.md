# EGFAnalysisTimeFreq_version_2024

**EGFAnalysisTimeFreq** is a MATLAB GUI software used for extract group and phase velocity dispersion curves from surface wave empirical Green’s function (EGF) or cross-correlation function (CF) from ambient noise. The dispersion analysis is based on an imaging analysis technique (Yao, van der Hilst, de Hoop, 2006, GJI; Yao et al., 2005, PEPI; Yao et al., 2011, C.R. Geoscience), which automatically traces the dispersion curve on the phase (or group) velocity–period image.

---

## Origin Version

The original stable version developed by **Huajian Yao** can be obtained as [**EGFAnalysisTimeFreq_version_2015**](https://yaolab.ustc.edu.cn/_upload/tpl/10/f0/4336/template4336/pdf/EGFAnalysisTimeFreq_version_2015.zip)  

---

## New Modifications in Version 2024

- Improved the previous automatic dispersion picking code, making it a more efficient and stable version.
- Provided a forward 3D phase/group velocity computation package based on CPS for 3D reference dispersion calculations. ([**SurfDispMap**](https://github.com/Ycpan-seis/SurfDispMap))
- Fixed several bugs present in the previous version.
- Updated the user manual to reflect all changes and enhancements.

---

## Documentation

For detailed instructions on program usage, please refer to the [manual](https://github.com/Ycpan-seis/EGFAnalysisTimeFreq_version_2024/blob/main/EGFAnalysisTimeFreq_Manual.pdf), which provide a complete description of the workflow, input/output formats, and underlying methodology.

Here, we only present the newly modified parts related to the automatic mode.”
> Users can click **3D Ref C/G Disper Great Circle**, then select the packaged .mat file(e.g., **RaylTB.mat**).
>
> The .mat file includes six MATLAB matrices:
>
> *disperT_m*, *lat_m*, *lon_m*, *disp3D_phase*, *disp3D_group* and *ref_range*
>
> *disperT_m*, *lat_m*, *lon_m*, *disp3D_phase* and *disp3D_group* correspond to the dispersion period, latitude, longitude, reference phase velocity, and reference group velocity for each data point, respectively. The format is latitude points * longitude points * number of periods.
>
> *ref_range* represents the tolerance range, with a format of number of periods * 2. (The first column is the period and the second column is reference values (percentage))

**The input .mat file can be prepared use [SurfDispMap](https://github.com/Ycpan-seis/SurfDispMap).**

In the automatic mode, the parameter `r_dcdt`, which constrains the slope of the dispersion curves, is very important. A reference value is provided, but it may need adjustment depending on the dataset. Users are encouraged to experiment with `r_dcdt` to achieve optimal results.


---

## References

- **Yao, H., van der Hilst, R.D., & de Hoop, M.V., 2006.** Surface-wave array tomography in SE Tibet from ambient seismic noise and two-station analysis: I - Phase velocity maps. *Geophys. J. Int.*, 166(2), 732–744. [doi:10.1111/j.1365-246X.2006.03028.x](https://doi.org/10.1111/j.1365-246X.2006.03028.x)

- **Yao, H., Xu, G., Zhu, L., & Xiao, X., 2005.** Mantle structure from inter-station Rayleigh wave dispersion and its tectonic implication in Western China and neighboring regions. *Phys. Earth Planet. Inter.*, 148(1), 39–54.

- **Yao, H., Gouedard, P., McGuire, J., Collins, J., & van der Hilst, R.D., 2011.** Structure of young East Pacific Rise lithosphere from ambient noise correlation analysis of fundamental- and higher-mode Scholte-Rayleigh waves. *Comptes Rendus Geoscience*, 343, 571–583. [doi:10.1016/j.crte.2011.04.004](https://doi.org/10.1016/j.crte.2011.04.004)
