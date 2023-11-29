import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
searchterms = pd.read_csv('searchterms.csv')
searchterms
platforms = searchterms[['Month','Android','iOS','macOS','Windows']]
platforms
plt.figure(figsize=(15, 8))
sns.lineplot(data=platforms, x='Month', y='Android', color='r', label='Android', marker='o')
sns.lineplot(data=platforms, x='Month', y='iOS', color='g', label='iOS', marker='o')
sns.lineplot(data=platforms, x='Month', y='macOS', color='b', label='macOS', marker='o')
sns.lineplot(data=platforms, x='Month', y='Windows', color='m', label='Windows', marker='o')
plt.xlabel('Months')
plt.ylabel('Values')
plt.title('Developer searches by operating system from January to December')
plt.show()
cloud = searchterms[['Month', 'AWS', 'AZURE', 'CloudFormation', 'GCP', 'IBM Cloud', 
                     'OpenStack', 'ORACLE Cloud', 'Terraform']]
cloud
plt.figure(figsize=(18, 10))
sns.lineplot(data=cloud, x='Month', y='AWS', color='b', label='AWS', marker='o')
sns.lineplot(data=cloud, x='Month', y='AZURE', color='g', label='AZURE', marker='o')
sns.lineplot(data=cloud, x='Month', y='CloudFormation', color='r', label='CloudFormation', marker='o')
sns.lineplot(data=cloud, x='Month', y='GCP', color='k', label='Google Cloud Platform', marker='o')
sns.lineplot(data=cloud, x='Month', y='IBM Cloud', color='c', label='IBM Cloud', marker='o')
sns.lineplot(data=cloud, x='Month', y='OpenStack', color='y', label='OpenStack', marker='o')
sns.lineplot(data=cloud, x='Month', y='ORACLE Cloud', color='m', label='ORACLE Cloud', marker='o')
sns.lineplot(data=cloud, x='Month', y='Terraform', color='orange', label='Terraform', marker='o')
plt.xlabel('Months')
plt.ylabel('Search count')
plt.title('Cloud developer search counts from January to December')
plt.show()
cybersecurity = searchterms[['Month','Arcsight', 'CyberArk', 'Darktrace', 'Nessus',
                            'Netskope', 'Nexpose', 'OWASP', 'PCI-DSS', 'Qualys', 'Splunk', 'Wireshark']]
cybersecurity
plt.figure(figsize=(18, 10))
sns.lineplot(data=cybersecurity, x='Month', y='Wireshark', color='b', label='Wireshark', marker='o')
sns.lineplot(data=cybersecurity, x='Month', y='Arcsight', color='g', label='Arcsight', marker='o')
sns.lineplot(data=cybersecurity, x='Month', y='CyberArk', color='r', label='CyberArk', marker='o')
sns.lineplot(data=cybersecurity, x='Month', y='Darktrace', color='k', label='Darktrace', marker='o')
sns.lineplot(data=cybersecurity, x='Month', y='Nessus', color='c', label='Nessus', marker='o')
sns.lineplot(data=cybersecurity, x='Month', y='Netskope', color='y', label='Netskope', marker='o')
sns.lineplot(data=cybersecurity, x='Month', y='Nexpose', color='m', label='Nexpose', marker='o')
sns.lineplot(data=cybersecurity, x='Month', y='OWASP', color='orange', label='OWASP', marker='o')
sns.lineplot(data=cybersecurity, x='Month', y='PCI-DSS', color='purple', label='PCI-DSS', marker='o')
sns.lineplot(data=cybersecurity, x='Month', y='Qualys', color='pink', label='Qualys', marker='o')
sns.lineplot(data=cybersecurity, x='Month', y='Splunk', color='darkgreen', label='Splunk', marker='o')
plt.xlabel('Months')
plt.ylabel('Search count')
plt.title('Cybersecurity job search counts from January to December')
plt.show()


