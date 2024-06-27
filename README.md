# ARES and SEDs, a tutorial.

Welcome. Here reside the Luberto et al. templates for SED fitting with EAZY.

The files are in the repo, as are tutorials showing how to do more stuff with it than running in native EAZY. With them we can recover full (predicted) SFHs, for instance.

There are a few ways you can use these templates. Here are a few use-cases:

## You want the z, mass, SFR fits and that's all:

This is the quick option, and all you need to do is download the templates. Choose if you want Lya or no Lya, follow the instructions by EAZY for how to use the new template set (really just putting it in the 'templates' directory in EAZY), and celebrate your succesful use of these templates!

Or if you want EAZY to run even faster, you can download the 'tempfilt' files for the template sets and run the EAZY instance with 'tempfilt=tempfilt_array', where 'tempfilt_array' is the file from here. I recommend just doing np.loadtxt() to load the file into your Python code. Doing this will skip the setup portion in EAZY (where it computes what the template set looks like as photometry and across z) and immediately go into the fitting procedure. It can save a lot of time.

To get the z, stellar mass, SFR at z observed, you go through EAZY itself, either in it's 'standard_output()' functionality or stuff like EAZY.zbest. Note that the SFRs INCLUDE the contribution from bursts, if you choose those templates.

## What about a deeper analysis on the SFR (either across z or dealing with the burstiness better)?

This makes a lot of sense considering the bursts in the templates are included in the SFR spit out in EAZY. For instance, if you want to know the burstiness of the galaxy, you need to know the galaxy contribution AND the burst contribution. The tutorial '[NAME]' shows you how to do this. You can also know what the SFR looks like throughout all z, as seen in '[NAME]'. 

You still have to run the EAZY code, as always, to get the fitting coefficients.

## Now, I just know there's more information to be extracted than what was presented in the paper...

Yep! This comes down to knowing the template set galaxies really well in ARES. You do follow the same steps above to use ARES to create the galaxy. Talk to Jordan Mirocha if you want to know more about ARES. There are some technical considerations that are tricky...like dust...which make it hard to get some parameters. Contact us if you have a question about that!

