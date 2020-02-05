Ansible Role: Kubespray
=========================

За основу взята роль: https://github.com/kubernetes-sigs/kubespray.git v2.12.0

Доработано
-----

- Установка docker `container-engine` из своих репозиториев

  См. блок в `roles/container-engine/docker/tasks/main.yml` к которому применено условие `use_custom_repositories | bool == false`:

  - `use_custom_repositories: true` - установка из репозитория, определенного в ОС.
  - `use_custom_repositories: false` - установка из репозитория, определенного в роли kubespray.

