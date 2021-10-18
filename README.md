# Abhinandan
web scaraping using googlecolab
import pandas as pd
import re
import requests
from bs4 import BeautifulSoup


url=f'https://sofifa.com/players'

# 10 pages

a = [0, 60, 120, 180, 240, 300, 360, 420, 480, 540]

for i in a:
  print(f'https://sofifa.com/players?offset={i}')

#Parameters

NAME = []
AGE = []
OVA = []
POT = []
TEAM_NAME = []
CONTRACT = []
VALUE = []
WAGE = []
TOTAL_STATS = []

for i in a:
 url='https://sofifa.com/players?offset={i}'

resp=requests.get(url)

soup=BeautifulSoup(resp.content,'lxml')

import pandas as pd
df=pd.DataFrame({"Name":NAME,
                 "Age":AGE,
                 "Overall Rating":OVA,
                 "Potential": POT,
                   "Team_Name": TEAM_NAME,
                   "Contract_Year": CONTRACT,
                   "Value(M)": VALUE,
                   "Wage(K)": WAGE,
                   "Total_Stats": TOTAL_STATS})
df.head() 
df.to_csv('fifa.csv')


df.head()

df.to_csv('fifa.csv')

soup

soup.prettify

arr=[]
for i in soup.findAll('td'):
  arr.append(str(i))

arr

arr[1]

  re.sub('^<td class="col col-pt" data-col="pt">.*">|<td class="col col-oa" data-col="oa"><span class="bp3-tag p p-76">|<td class="col-name">| rel="nofollow|É. Mendy</div></a>|<span class="pos pos0">GK|</span></td>|<td class="col-name">|\n<a class="tooltip" data-tooltip=|M. Sarr</div></a>|<td class="col col-tt" data-col="tt">|</div>\n</div>\n</td>|<td class="col col-ae" data-col="ae">|<span class="bp3-tag p">|<td class="col col-oa" data-col="oa"><span class="bp3-tag p p-74">|<td class="col col-vl" data-col="vl">|</td>|\n<div class="bp3-text-overflow-ellipsis"><figure class="avatar avatar-sm transparent">\n<img alt="" class="team" data-root="https://cdn.sofifa.com/teams/" data-src="https://cdn.sofifa.com/teams/5/30.png" data-srcset="https://cdn.sofifa.com/teams/5/60.png 2x, https://cdn.sofifa.com/teams/5/90.png 3x" data-type="team" src="https://cdn.sofifa.com/teams/notfound_30.png"/>\n</figure>\n<a href="/team/5/chelsea/">Chelsea</a><div class="sub">\n|href="/player/235454/malang-sarr/220007/">|https://cdn.sofifa.com/flags/fr.png|<div class="bp3-text-overflow-ellipsis">|<span class="pos pos5">CB</span></a>|" src="" title="France"/>||<img alt="" class="flag|https://cdn.sofifa.com/flags/fr@2x.png 2x, https://cdn.sofifa.com/flags/fr@3x.png 3x||ST|<span class="pos pos25">|P. Daka</div></a>|href="/player/241202/patson-daka/220007/">|<td class="col-avatar"><figure class="avatar">\n<img alt="" class="player-check" data-root="https://cdn.sofifa.com/players/" data-src="https://cdn.sofifa.com/players/234/642/22_60.png" data-srcset="https://cdn.sofifa.com/players/234/642/22_120.png 2x, https://cdn.sofifa.com/players/234/642/22_180.png 3x" data-type="player" id="234642" src="https://cdn.sofifa.com/players/notfound_0_60.png"/></figure>|</span></a>|href="/player/234642/edouard-mendy/220007/">|/players?pn=0| src="" title="Senegal"|data-src="https://cdn.sofifa.com/flags/sn.png"| data-srcset="https://cdn.sofifa.com/flags/sn@2x.png 2x, https://cdn.sofifa.com/flags/sn@3x.png 3x"|<td class="col col-oa" data-col="oa"><span class="bp3-tag p p-83">| data-src="https://cdn.sofifa.com/flags/zm.png" data-srcset="https://cdn.sofifa.com/flags/zm@2x.png 2x, https://cdn.sofifa.com/flags/zm@3x.png 3x" src="" title="Zambia"/>|<td class="col col-oa" data-col="oa"><span class="bp3-tag p p-59">|<figure class="avatar avatar-sm transparent">\n<img alt="" class="team" data-root="https://cdn.sofifa.com/teams/" data-src="https://cdn.sofifa.com/teams/47/30.png" data-srcset="https://cdn.sofifa.com/teams/47/60.png 2x, https://cdn.sofifa.com/teams/47/90.png 3x" data-type="team" src="https://cdn.sofifa.com/teams/notfound_30.png"/>\n</figure>\n<a href="/team/47/ac-milan/">AC Milan</a><div class="sub">|href="/player/20801/c-ronaldo-dos-santos-aveiro/220007/">| data-srcset="https://cdn.sofifa.com/flags/pt@2x.png 2x, https://cdn.sofifa.com/flags/pt@3x.png 3x"|"https://cdn.sofifa.com/flags/pt.png" src="" title="Portugal"/>|<a href="|<a href="/players?pn=27"|</a>|<span class="pos pos27">|<span class="pos pos27">|<td class="col col-oa" data-col="oa"><span class="bp3-tag p p-91">|"https://cdn.sofifa.com/teams/"||"team"|data-root=|data-src=|data-type=|/team/11/manchester-united/">Manchester United|</figure>|" class="team"|<img alt="|src="https://cdn.sofifa.com/teams/notfound_30.png"/>|"https://cdn.sofifa.com/teams/11/30.png"|<figure class="avatar avatar-sm transparent">| data-srcset="https://cdn.sofifa.com/teams/11/60.png 2x, https://cdn.sofifa.com/teams/11/90.png 3x"|<span class="pos pos14">|href="/player/233927/lucas-tolentino-coelho-de-lima/220007/">|src="" title="Brazil"/>| </div>"|Lucas Paquetá|"https://cdn.sofifa.com/flags/br.png" data-srcset="https://cdn.sofifa.com/flags/br@2x.png 2x, https://cdn.sofifa.com/flags/br@3x.png 3x"|<div class="sub">|\n|<td class="col col-wg" data-col="wg">|<span class="pos pos7">LB</span></a></td>','',arr[300])
  

76
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              ])
