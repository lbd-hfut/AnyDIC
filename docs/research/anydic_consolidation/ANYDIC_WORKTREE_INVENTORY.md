# 最终Worktree台账

> 公开发布副本：本机路径已符号化，操作台账按隐私范围精简；科学结论沿用冻结源文档。修改及历史验证范围见 [PUBLICATION_NOTICE](PUBLICATION_NOTICE.md)。

注册来源：主仓库 `git worktree list --porcelain`。初始39个，最终2个。主项目从未列入删除目标。所有38个额外checkout经独立 common-dir/branch/HEAD核查；完整源文件（path/size/SHA256/Git分类）、ignored/untracked明细、全部Markdown/PDF以及源分支/HEAD在外部逐树manifest；本机JSON保存校验过的manifest指纹。

| 原路径 | 阶段 | 原分支 | 原HEAD完整SHA | runs bytes | checkpoint数 | 归档/最终状态 |
| --- | --- | --- | --- | --- | --- | --- |
| ${ANYDIC_REPOSITORY} | AnyDIC | main | 5c0ec91458ab6dbe5f485a78e453da5061099a62 | 216512 | 0 | MAIN_PROTECTED |
| ${ANYDIC_WORKTREES}/anydic-c11-matching-repair | C11 | experiment/anydic-c11-matching-repair | 0ac7d6659b84e2ef39072e45e88f06e3a38fce51 | 2671646772 | 7 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-c12-cross-resolution | C12 | experiment/anydic-c12-cross-resolution | 97cecd6fd3ad7b424502cfdbc0cdc09ccdee4176 | 4708018916 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-c13-scale-aware | C13 | experiment/anydic-c13-scale-aware | c9270878b1d4e463d5823da1c92c859fef7ad3e1 | 5903001129 | 5 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-c14-nonrotation | C14 | experiment/anydic-c14-nonrotation-cross-scale | f2dbcfe8120b04ffcc30a32eba2675c865df715d | 6368038546 | 1 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-c15-full-frame | C15 | experiment/anydic-c15-full-frame-training | c960a39379ea10d5f65825a89f4bc29e69832746 | 5038319387 | 6 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-c16-native-update-stability | C16 | experiment/anydic-c16-native-update-stability | caba509f21de6f698c01e8ef685851c0b2dca887 | 5257307386 | 0 | ACTIVE_PROTECTED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c0 | C0 | experiment/anydic-low-v3-c0-generalization | 335284bf24a1ec252901ed6b1d662543cf05acc5 | 892993364 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c1 | C1 | experiment/anydic-low-v3-c1-convergence | d760af109a22010b758b91c7336d939cfe6cdad3 | 35072831991 | 12 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c10 | C10 | experiment/anydic-low-v3-c10-support-aware | 40ab87ed1ae3478cc32d5121b84824c014616689 | 1216947757 | 6 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c1g | C1G | experiment/anydic-low-v3-c1g-affine | 837a2cafa000f9953172693770a1ac9a2b1ab605 | 175463548 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c2 | C2 | experiment/anydic-low-v3-c2-final | bf6e0d29cdd870c47d65bf81696beddf0c31edcd | 538953074 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c3a | C3A | experiment/anydic-low-v3-c3a-equivariant | bd8f347d7b7097fdc65697b4226b921030f0cf60 | 13035681978 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c3d | C3D | experiment/anydic-low-v3-c3d-candidate-fate | 735acc53a962922d9ba357eb05a067b8b68819c3 | 18469868446 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c3e | C3E | experiment/anydic-low-v3-c3e-f4-multihypothesis | 6f23a9424d3d1c7f662c1d9d5e80a86c20361225 | 548463687 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c4 | C4 | experiment/anydic-low-v3-c4-identifiability | c033fc1ea98e8f56c8bbec3e090e118c6bd66ffb | 1117 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c4b | C4B | experiment/anydic-low-v3-c4b-bidirectional | dad1a0616efa4d375caa030297bb3142842cbc7a | 305812626 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c5 | C5 | experiment/anydic-low-v3-c5-local-refinement | 56303e977cef3e4d8b2de96d51ebdbce92ba8649 | 67090113 | 1 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c5r | C5R | experiment/anydic-low-v3-c5r-recheck | 5df6219f0c732cec1fab8f1279661b9fa732a242 | 4540344 | 4 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c6 | C6 | experiment/anydic-low-v3-c6-information-audit | 7af849d8f4e1073a82c29604d4b0010cf236ff0d | 8935036027 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c7 | C7 | experiment/anydic-low-v3-c7-local-feature | 08747426ee2fcfe89a16864312606e0321338f85 | 2715533551 | 5 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c8 | C8 | experiment/anydic-low-v3-c8-pair-conditioned | d6506f3b24d86154bde45205cc8bb84de1b0b434 | 21072406 | 1 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c9 | C9 | experiment/anydic-low-v3-c9-real-validation | 0d802df1bdd5c3456072d43e076efa3300ac8e46 | 1117 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c9b | C9B | experiment/anydic-low-v3-c9b-dic-challenge | 859d53e1b7e769f15e4ac91d397de56c4804f5ba | 108587453 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-c9c | C9C | experiment/anydic-low-v3-c9c-observability | 594678f2315b1b2a2a948ef624d27145c1690648 | 882782077 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-d2 | D2 | diagnostic/low-v3-r1-failure-mechanism | 52c7981f4b754fcfd2b97a8b8cbeaaadb5200d0f | 894671379 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-d3 | D3 | experiment/anydic-low-v3-d3-dual-phase | ae59a4b74bb975be5d7da68c26ae24d2a6b961d3 | 1362047203 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-d4-f8net | D4 | experiment/anydic-low-v3-d4-f8net | 1b8d72fe82150b8ca1c171799ce0664e0930dcfa | 15466321104 | 28 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-d5 | D5 | diagnostic/anydic-low-v3-d5 | f2a20057e93595e7a98243812cc817d64443cf15 | 1947168596 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-d6a-f4net | D6A | experiment/anydic-low-v3-d6a-f4net | 02ca1ab8e16d9bf432063816e2011840293d51ed | 29278912889 | 25 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-d6b-joint | D6B | experiment/anydic-low-v3-d6b-joint | 7bef21a6b119c051f0805031dc18a3229d212497 | 31825113183 | 8 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-f8 | anydic-low-v3-f8 | experiment/anydic-low-v3-f8 | 2dee12c21d8cfcf2cde4088daeb2d613b0c8eeef | 1819619271 | 5 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-f8-r1 | anydic-low-v3-f8-r1 | experiment/anydic-low-v3-f8-r1 | e79619081a737b5d39d1dcac65c81e440b5b3ab0 | 2763326424 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-low-v3-prospective | anydic-low-v3-prospective | experiment/anydic-low-v3-prospective | ef942815a618ef9d5920cf92576b630cf8698171 | 1266980233 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-medium-gmflow-coarse | anydic-medium-gmflow-coarse | experiment/anydic-medium-gmflow-coarse | d74511567de499f53f8b3ce83534b137c2e22603 | 167794 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-medium-m2-gmflow-lightweight | M2 | experiment/anydic-medium-m2-gmflow-lightweight | 2f0f2c4b49faa9ccd489cebbebd2b7b821782fd3 | 1117 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-medium-m3-continuous-e8 | M3 | experiment/anydic-medium-m3-continuous-e8 | b45668d3fe41a941be0a189e6f4e2bbe26e824ac | 14220775 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-medium-m4-routing | M4 | experiment/anydic-medium-m4-routing | 1d53d4cbd37cb8fe3defd69e2e7fc1d27e3f23b5 | 1117 | 0 | REMOVED_VERIFIED |
| ${ANYDIC_WORKTREES}/anydic-medium-m5-prospective | M5 | experiment/anydic-medium-m5-prospective | d4c0c6c42cc90c1f05a52b3f0ed4561b3ed4c857 | 1117 | 0 | REMOVED_VERIFIED |

## 安全审计

无旧worktree的tracked/staged或常规untracked修改；clean并未作为ignored数据可删除依据。所有不可由Git恢复的文件、环境与外部仓库均保留并全SHA256校验。C16活动shell/VS Code保留；未终止任何其他任务。源清单的少量untracked分类文件位于忽略的研究父目录，已与ignored资产一并归档，未丢弃。

主目录原始 `case/dic_challenge/` 最初未追踪；最终通过本机 `.git/info/exclude` 中唯一新增 `/case/dic_challenge/` 规则保持常规Git status clean，原文件未移动、未删除、未加入Git。该规则只改变Git显示/准入，不改变数据生命周期；完整原始case元数据仍在保护清单。主目录既有交互Codex/shell未终止，同HEAD创建新分支时生产源码无改变。
