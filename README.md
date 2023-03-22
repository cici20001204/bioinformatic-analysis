# bioinformatic-analysis
import matplotlib.pyplot as plt
import numpy as np
x1 = np.array([3.9,1.6,1.4,0,0,1.4,1.3,1.2,2.4,0,1.2,0,1.1,0,0,1,1])
x2 = np.array([0,0,0,0.7,0.7,0,0,0,0,0.7,0,0.9,0,0.9,0.9,0,0])
bar_labels = ['UVM','KIRC','LUSC','BRCA','LIHC','GBM','STAD','BLCA',
              'KICH','ACC','COAD','KIRP','OV','CESC','DLBC','PAAD','CHOL']
y_pos = np.arange(len(x1))
plt.barh(y_pos,x1,color = 'g',alpha = 0.5)
plt.barh(y_pos,-x2,color = 'b',alpha = 0.5)
plt.xlim(-max(x2)-1,max(x1)+1)
plt.ylim(-1,len(x1))
plt.xticks(np.arange(-2, 6, step=1),[2,1,0,1,2,3,4,5])
plt.yticks(y_pos,bar_labels)
plt.ylabel('HR')
plt.title('Biocarta_comp_pathway')
plt.show()
