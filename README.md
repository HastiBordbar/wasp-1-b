# wasp-1-b
The Photometry study of the exoplanet “wasp-1 b”
import numpy as np
import matplotlib.pyplot as plt                                         
from astropy.io import fits                                             

from astropy.table import Table


tb = Table.read('OutTable11.fits')  


deltamag = -2.5 * np.log10(tb['flux_WASP-1']/tb['flux_TYC2265_54_1'])

#print(np.polyfit(tb['TimeHJD'],deltamag,20))
