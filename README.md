# ICL Publications

This repository host the publications from ICL. The data is used on [this page](http://icontrol.ri.cmu.edu/publication/publication.html).


# Data Format

In addition to including normal BibTeX fields such as `key`, `author`, `title`, `year`, we added the following entries:
1. `index`: a unique number following a character. The character specifies catagories and the number follows chronical order. We use the following categories.
```
C: conference
J: journal
B: book/book chapter
T: thesis
W: workshop
U: unpublished
P: Pattern
```
For example, `C50` is the 50th conference paper published by ICL members.

2. `url`: a link to the publically accessible preprint of the paper.

3. `link`: a link to the publisher's site, e.g., IEEE Xplore. ICL's publication page will first use `url` with the `Preprint` button, and if `url` does not exist, it will use `link` with the `Link` button.

4. `repository`: a link to the code associated with the paper.

5. `video`: a link to the YouTube video associated with the paper. Note we need to use `embed` link:
```
https://www.youtube.com/embed/5tsSdKkTc4M
```
instead of `watch` link
```
https://www.youtube.com/watch?v=5tsSdKkTc4M
```

6. `info`: additional information/resources for the paper, which could be the project webpage, the poster, the slides, the supplementary material, etc. Note only one link can be provided in this entry. It will be linked to the `Page` button on the ICL publication page.

7. `abstract`: abstract of the paper, which will be displayed in a drop down window on the ICL publication page.

8. `award`: if this paper receives award, add the award information here.

9. `notes`: additional information for the paper, which won't be directly linked on the ICL publication page, but is visible inside the BibTex record if user clicks the `Cite` button. If a conference/journal paper is previously presented at a workshop or other non-archieval venue, only include the BibTex record for the archieval version, and then add a note for its previous publication(s). Example:

```
@inproceedings{lin2024nnsysbench,
  index = {C85},
  title={{NN}4SysBench: Characterizing Neural Network Verification for Computer Systems},
  author={Shuyi Lin and Haoyu He and Tianhao Wei and Kaidi Xu and Huan Zhang and Gagandeep Singh and Changliu Liu and Cheng Tan},
  booktitle={The Thirty-eight Conference on Neural Information Processing Systems Datasets and Benchmarks Track},
  year={2024},
  url={https://openreview.net/forum?id=mhjRudcHcB},
  notes={Also presented at ICML Workshop on Formal Verification of Machine Learning 2022 under the title "Characterizing Neural Network Verification for Systems with NN4SYSBENCH". Link: https://naizhengtan.github.io/doc/papers/characterizing22haoyu.pdf}
}
```
10. `teaser`: an image or gif to highlight the work. This will be displayed in a drop down window on the ICL publication page.

Additionally, we use the following conventions:

1. Conference publications need to use `@inproceedings` where the venue should be listed in `booktitle`. Journal publications need to use `@article` where the venue should be listed in `journal`. Thesis should use `@phdthesis` with the field `booktitle={PhD Thesis}`. Book chapters should use `@incollection`. Book should use `@book` and the venue should be listed in `publisher`. Patent should use `@misc` with the field `booktitle={US Patent App. ###}`. 

** Todo: Still need to decide the rule for workshop papers. For now, they are either using `@article` or `@inproceedings`.

2. Venues. Do not include the year and the short name in the venue. The conventions are shown below (put the entries after `:` to either `booktitle` or `journal`): 

```
IROS: IEEE/RSJ International Conference on Intelligent Robots and Systems
ICRA: IEEE International Conference on Robotics and Automation
DSCC: Dynamic Systems and Control Conference
ACC: American Control Conference
ITSC: IEEE International Conference on Intelligent Transportation Systems
IV: IEEE Intelligent Vehicles Symposium
SC-L: Systems & Control Letters
SICON: SIAM Journal on Control and optimization
CCTA: IEEE Conference on Control Technology and Applications
T-IV: IEEE Transactions on Intelligent Vehicles
ICARCV: International Conference on Control, Automation, Robotics and Vision
CDC: IEEE Conference on Decision and Control
L4DC: Learning for Dynamics and Control Conference
TECS: ACM Transactions on Embedded Computing Systems
IFAC: IFAC World Congress
RA-L: IEEE Robotics and Automation Letters
CORL: Conference on Robot Learning
WAFR: International Workshop on the Algorithmic Foundations of Robotics
ISFA: International Symposium on Flexible Automation
AIM: IEEE/ASME International Conference on Advanced Intelligent Mechatronics
CPHS: IFAC Workshop on Cyber-Physical Human Systems
RSS: Robotics: Science and Systems
```

** Todo: create a more automatic and consistent way to reference different venues.

3. The key for each publication should be created as 
```
last name of the first author + year of publication + first word of the title + indexing if the first three entries cannot uniquely identify the paper
```
Note that some paper may be on arXiv in an earlier year than its actual publication year. In this case, we should still update the citation key to be the actual publication year. For unpublished papers, we can use the year when it appears on arXiv.

## Issues

1. Missing all master thesis
2. Missing detailed information for publications starting in 2022

