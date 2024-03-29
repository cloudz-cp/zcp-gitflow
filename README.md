# zcp-gitflow

## Branch 
- develop, main, feature, hotfix만 사용
- main, develop에 직접적인 commit은 금지
- feature, hotfix의 commit 메세지는 자유롭게 작성
- feature 및 hotfix는 merge 후 삭제한다
- 브랜치명
  - feature: feature/{issue-number}-blabla
  - hotfix: hotfix/{issue-number}-blabla
- setting rules
  - github > Settings > Branches > Branch protection rules > Add rule
  - Main/Develop branch에 rule 적용
  - ![스크린샷 2021-12-06 오후 5 07 10](https://user-images.githubusercontent.com/56831448/144809987-e607037e-9174-44d7-8e6b-af5cf5cba36a.png)
- setting default branch
  - default branch를 develop으로 변경 
  - issue & pr template은 default branch를 기준으로 적용되기 때문에 필요 
  ![스크린샷 2021-12-08 오후 5 39 17](https://user-images.githubusercontent.com/56831448/145176280-24be282f-6108-4011-b667-8954e0d24bfd.png)
  
## PR & Issue
- issue 없는 PR은 없다
- issue, PR, Release Note가 연결되기 때문에, issue의 naming에 신경쓴다
- issue와 PR은 template 양식에 맞춘다
- PR은 아래와 같은 상황을 제외하고는 본인 제외 1명 이상의 Review를 받는다
  - Document, manifest, config, 주석에 대한 수정만을 진행하는 경우
  - Slack을 통해 파트 전체에게 리뷰없이 Merge하겠다는 의사를 밝힌경우
- PR의 Merge는 스스로 한다 
- github의 merge는 [Create a merge commit] & [Squash and merge]만 사용
  - [Create a merge commit]: develop-branch와 main-branch간의 merge시에 사용
  - [Squash and merge]: 임시-branch와 develop-branch간의 merge시에 사용
- issue명
  - [kind] issue 이름 
  - ex) [bug] Cannot access zcp-console 
- PR명
  - issue의 첫번째 PR: `Resolved#{issue_number}-{issue 이름}`
  - issue의 두번째 PR: `Re-Resolved#{issue_number}-{수정사항요약}`
  - ...
  - issue의 N번째 PR: Re-Resolved#{issue_number}-{수정사항요약}

## Detail
- https://docs.google.com/presentation/d/1_NnesPXMfjXXeKcebJzY-XAes2WzagwVMeg9OwFPiT0/edit?usp=sharing

