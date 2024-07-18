# Kubestronaut Roadmap

This is a step-by-step guide on how to become a Kubestronaut, with links to relevant learning resources.

If you want to watch a video version of this roadmap, you can find it [here](https://www.youtube.com/watch?v=Xjmqi8vt3Rg).

## The program

The [Kubestronaut program](https://www.cncf.io/training/kubestronaut/) recognises community leaders who have consistently invested in their ongoing education and grown their skill level with Kubernetes. Individuals who have successfully passed every CNCF’s Kubernetes certifications – CKA, CKAD, CKS, KCNA, KCSA – will receive the title of “Kubestronaut”, as well as these additional benefits:

* An exclusive Kubestronaut jacket to show off your elite status
* A Credly badge to showcase your expertise
* Access to the dedicated / private Kubestronaut Slack channel and mailing list
* Coupons for 50% off five certifications each year – for yourself or to share
* 25% off three CNCF events a year

## Certifications

* CKA, CKS, CKAD:
  * Duration: 2h
  * Questions: 15-20 performance-based
* KCNA, KCSA:
  * Duration: 1h30
  * Questions: 60 multiple-choice

My recommended order to take the certifications:

* If you have some experience and knowledge on Kubernetes, containers and cloud-native ecosystem:
  * KCNA -> CKA -> CKAD -> CKS -> KCSA
  * Rationale: Starting with KCNA provides a solid foundation in Kubernetes and the cloud-native ecosystem. The CKA certification will deepen your understanding of cluster administration. Next, CKAD will help you build, deploy and manage workloads on Kubernetes. Studying for CKS will enhance your knowledge of Kubernetes security, which will make it easier to grasp theoretical concepts covered in KCSA.

* If you have some knowledge on cloud-native ecosystem, but don't have too much experience with Kubernetes:
  * KCNA -> CKAD -> CKA -> KCSA -> CKS
  * Rationale: Begin with KCNA to establish a fundamental understanding of Kubernetes and cloud-native principles. Move on to CKAD to learn how to develop and deploy applications in Kubernetes. Then, study for CKA to gain advanced skills in Kubernetes administration. KCSA will give you insights into theoretical content of cloud-native security, and finally, CKS will focus out on kubernetes security, leveraging the knowledge gained from the previous certifications.

> CKA is a pre-req for CKS.

In my opinion, if we order by exam difficulty, we have:

CKS (hard one) -> CKA -> KCSA -> CKAD -> KCNA (easy one)

## General tips

For all exams:

* Always be present 30min before the exam start to do the checkin

* Reliable internet connection and a good webcam (if the proctor can't read your ID during the checkin you won't be able to do the exam)

* If you can't answer a question quickly, mark it as flagged and move on. Try solving the easier questions first to gain more confidence and then work on solving the other questions.

For CKA, CKAD, CKS:

* Be fast with kubectl

* Do not memorize YAML manifest syntax. Use imperative commands (you can do 80% of the exam with imperative commands). Ex = create pods, deploys, daemonsets, serviceaccounts, role, rolebinding, service; If you need to, check the documentation and copy and paste the yaml manifests.

* Always check the context in which you are running kubectl commands, as there are many clusters.

* Spent 1min on env setup. The exam environment already have the alias for "k=kubectl". Also `.vimrc` is configured with `shiftwidth=2; expandtab=true; tabstop=2`. If you want you can configure just:

```bash
export do="--dry-run=client -o yaml"
# k create deploy nginx --image=nginx $do

export now="--force --grace-period 0"
# k delete pod abc $now
```

* Copy/paste won't work as usual:
  * You can use the menu from right click
  * ctrl+shift+c / ctrl+shift+v
  * Click-copy from the instructions

* You should be familiar with Kubernetes documentation as well, so spent some time reading and searching through k8s docs. Try to remember pages with examples of manifests (e.g., pv, pv, network policy, ingress) so you can copy/paste faster.

## Kubernetes and Cloud Native Associate (KCNA)

[KCNA](https://training.linuxfoundation.org/certification/kubernetes-cloud-native-associate/) will test your knowledge and skills in Kubernetes and the wider cloud native ecosystem. In my opinion, is the easiest one. *Pass score is 75%*.

Study but not limited to the following:

* Overview of container orchestration
* Kubernetes fundamentals
* Cloud Native Architectures
* Concepts of CI/CD, GitOps
* Some knowledge of the CNCF projects
* Concepts of observability

Recommended Labs and resources:

* <https://www.linkedin.com/pulse/how-ace-kcna-kubernetes-cloud-native-associate-exam-keratishvili-mwhwf/>

## Kubernetes and Cloud Native Security Associate (KCSA)

[KCSA](https://training.linuxfoundation.org/certification/kubernetes-and-cloud-native-security-associate-kcsa/) will test your understanding of the baseline security configuration of Kubernetes clusters to meet compliance objectives, including the ability to harden security controls, test and monitor the security, and participate in assessing security threats and vulnerabilities.

In my opinion, this certification is very hard if you don't have kwnoledge on security fundamentals. *Pass score is 75%*.

Study but not limited to the following:

* 4Cs of Cloud Native Security
* control-plane protection
* admission Controllers
* auditing
* network Policies
* read the Cloud Native Security whitepaper

Recommended Labs and resources:

* <https://itnext.io/how-to-ace-kcsa-kubernetes-and-cloud-native-security-associate-exam-c9fae3f5c6a1>

## Certified Kubernetes Administrator (CKA)

[CKA](https://training.linuxfoundation.org/certification/certified-kubernetes-administrator-cka/) will test your skills, knowledge, and competency to perform the responsibilities of Kubernetes administrators.

In my opinion, it's the most important certification. A score of 66% or above must be earned to pass.

Study and practice but not limited to the following:

* how to perform etcd backup/restore
* how to cluster setup/upgrade with kubeadm
* creating pv, pvc and mounting volumes into pods.
* multi-containers in a pod
* nodeSelector, affinity
* taints, tolerations
* network policies
* services and ingresses
* pods, deployments
* kubelet troubleshooting
* control-plane components troubleshooting

Recommended Labs and resources:

* <https://killercoda.com/killer-shell-cka>
* <https://github.com/chadmcrowell/CKA-Exercises>
* <https://devopscube.com/cka-exam-study-guide/>
* <https://www.youtube.com/playlist?list=PL7bmigfV0EqS6WxgWlH-p4dhkfuwcZ6-E>

## Certified Kubernetes Application Developer (CKAD)

[CKAD](https://training.linuxfoundation.org/certification/certified-kubernetes-application-developer-ckad/) will test your ability to design, build, and deploy cloud-native applications using Kubernetes.

In my opinion, it is the easiest one. To pass, you must earn a score of 66% or above.

Study and practice but not limited to the following:

* build container images with Docker/Podman
* create pods, deployments, daemonsets, cronjobs
* blue/green deployments
* helm to deploy packages
* probes and healthchecks
* create ingress, service
* create secrets, configmaps

Recommended Labs and resources:

* <https://killercoda.com/killer-shell-ckad>
* <https://devopscube.com/ckad-exam-study-guide>

## Kubernetes Security Specialist (CKS)

[CKS](https://training.linuxfoundation.org/certification/certified-kubernetes-security-specialist/) will test your skills, knowledge, and competence on a broad range of best practices for securing container-based applications and Kubernetes platforms during build, deployment and runtime.

In my opinion, it is the most difficult one. To pass, you must earn a score of 67% or above.

Study and practice but not limited to the following:

* Be comfortable with changing control-plane components
* CIS benchmarks
* Know how to use tools like Falco, Sysdig, Tracee, Trivy
* Be comfortable with create and use ImagePolicyWebhook
* Setup audit policy
* Create Network policies
* Configure Security context for pod or container
* Create ServiceAccounts
* RBAC authorization

Recommended Labs and resources:

* <https://www.youtube.com/watch?v=d9xfB5qaOfg>
* <https://killercoda.com/killer-shell-cks>
* [Cloud Native Security Whitepaper](https://www.cncf.io/wp-content/uploads/2022/06/CNCF_cloud-native-security-whitepaper-May2022-v2.pdf)
* <https://github.com/walidshaari/Certified-Kubernetes-Security-Specialist>
* <https://github.com/ViktorUJ/cks>
