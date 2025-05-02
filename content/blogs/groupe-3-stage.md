---
title: "Stage 3S Sécurité"
date: 2025-04-09T19:53:33+05:30
draft: false
author: "Jarod PAUCHET"
tags:
  - Stage
  - 3S Sécurité
  - Groupe-3
image: /images/3Sreduce.png
description: "Retour sur mon stage chez 3S Sécurité : cybersécurité, supervision et automatisation."
toc: true
mathjax: true
---

## 🏢 Présentation de l’entreprise

> - **Nom :** *3S Sécurité - Groupe-3*
> - **Secteur d’activité :** *Sécurité des systèmes d’information*
> - **Localisation :** *38 Rue Maxime Guillot BP 50007, 21300 Chenôve*
> - **Date de Création :** *Fondée en 2020*
> > ### À propos de 3S Sécurité
> > ***3S Sécurité*** est une entreprise spécialisée dans la **protection des infrastructures informatiques**. 
>  
> > Elle accompagne les entreprises dans la sécurisation de leurs systèmes et la mise en place de solutions adaptées à leurs besoins.

---

## 🎯 Objectifs du stage

> L’objectif de mon stage était de participer à des projets liés à la **cybersécurité**, à la **supervision** et à l’**automatisation**.
>
> Développer mes compétences techniques en environnement professionnel
> 
> Participer à l'amélioration du SI de 3S Sécurité

---

## 🛠️ Missions réalisées

J’ai intégré une équipe technique chargée de déployer, sécuriser et optimiser une infrastructure réseau.

> - **Déploiement automatique de machines virtuelles clientes avec Ansible.**
> - **Création de playbooks Ansible personnalisés.**
> - **Mise en place de serveurs de supervision avec cAdvisor.**
> - **Audit de sécurité des machines.**
> - **Renforcement de la sécurité (hardening) des serveurs Linux.**
> - **Création de requêtes de supervision (queries) pour analyser le flux de données.**
> - **Configuration de switchs réseaux.**
> - **Participation au dépannage des clients.**

---


## ✅ Bilan

> Ce stage m’a permis de découvrir des domaines avancés comme la cybersécurité, la supervision et l’automatisation.
>
> J’ai pu mettre en pratique mes connaissances, approfondir mes compétences techniques, et développer ma rigueur dans un environnement exigeant. Ce stage a renforcé mon intérêt pour les métiers liés à la sécurité des systèmes d’information.

---

## 🔗 Annexes

> Voici un apercu de m'a collection **Ansible** pour déployer **FluentBit**
>
> Extrait de Fluentbit.yml
```
---
- name: Déployer Fluent Bit
  hosts: localhost
  become: yes
  vars_files:
    - /vars_files/influxdb_credentials.yml
  roles:
    - install_fluentbit  # Le rôle pour installer Fluent Bit
    - config_fluentbit   # Le rôle pour configurer Fluent Bit
    - restart_fluentbit  # Le rôle pour redémarrer Fluent Bit
```

> Extrait du rôle install_fluentbit
```
---
# Ajouter le dépôt Fluent Bit pour Debian
- name: Ajouter la clé GPG de Fluent Bit
  ansible.builtin.apt_key:
    url: https://packages.fluentbit.io/fluentbit.key
    state: present

- name: Ajouter le dépôt Fluent Bit pour Debian
  ansible.builtin.apt_repository:
    repo: "deb https://packages.fluentbit.io/debian/buster stable main"
    state: present
    filename: fluentbit

# Installer Fluent Bit
- name: Installer fluent-bit
  ansible.builtin.apt:
    name: fluent-bit
    state: present
    update_cache: yes

# Check si Fluent Bit est démarrer
- name: Démarrer Fluent Bit
  ansible.builtin.service:
      name: fluent-bit
      state: started
      enabled: yes
```

---

# Soutenance de stage

👉 [Voir le diaporama en plein écran](/slides/Soutenance-3S.html)

<iframe src="/slides/Soutenance-3S.html" width="100%" height="600px" style="border:none;"></iframe>
