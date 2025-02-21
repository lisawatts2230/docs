---
title: Restringir o tráfego de rede para a sua empresa
shortTitle: Restringir tráfego de rede
intro: Você pode usar um IP permitir que a lista restrinja o acesso ao seu negócio a conexões a partir de endereços IP especificados.
versions:
  ghae: '*'
type: how_to
topics:
  - Access management
  - Enterprise
  - Fundamentals
  - Networking
  - Security
redirect_from:
  - /admin/configuration/restricting-network-traffic-to-your-enterprise
---

## Sobre listas de permissões de IP

Por padrão, os usuários autorizados podem acessar sua empresa a partir de qualquer endereço IP. Os proprietários de empresas podem restringir o acesso a ativos pertencentes a organizações na conta corporativa, configurando uma lista de permissão de endereços IP específicos. {% data reusables.identity-and-permissions.ip-allow-lists-example-and-restrictions %}

{% data reusables.identity-and-permissions.ip-allow-lists-cidr-notation %}

{% data reusables.identity-and-permissions.ip-allow-lists-enable %} {% data reusables.identity-and-permissions.ip-allow-lists-enterprise %}

Você também pode configurar endereços IP permitidos para uma organização individual. Para obter mais informações, consulte "[Gerenciar endereços IP permitidos para a sua organização](/organizations/keeping-your-organization-secure/managing-allowed-ip-addresses-for-your-organization)".

Por padrão, as regras do grupo de segurança de rede do Azure (NSG) deixam todo o tráfego de entrada aberto nas portas 22, 80, 443 e 25. Proprietários de empresa podem entrar em contato com {% data variables.contact.github_support %} para configurar as restrições de acesso para sua instância.

Para restrições no nível da instância que usam o Azure NSGs, entre em contato com {% data variables.contact.github_support %} com os endereços IP que devem ter permissão para acessar a sua instância corporativa. Especifica os intervalos de endereços usando o formato CIDR padrão (Encaminhamento sem Classe entre Domínios). {% data variables.contact.github_support %} irá configurar as regras de firewall apropriadas para sua empresa para restringir o acesso à rede por meio de HTTP, SSH, HTTPS e SMTP. Para obter mais informações, consulte "[Receber ajuda de {% data variables.contact.github_support %}](/admin/enterprise-support/receiving-help-from-github-support)".

## Adicionar endereços IP permitidos

{% data reusables.identity-and-permissions.about-adding-ip-allow-list-entries %}

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.settings-tab %}
{% data reusables.enterprise-accounts.security-tab %}
{% data reusables.identity-and-permissions.ip-allow-lists-add-ip %}
{% data reusables.identity-and-permissions.ip-allow-lists-add-description %}
{% data reusables.identity-and-permissions.ip-allow-lists-add-entry %}
{% data reusables.identity-and-permissions.check-ip-address %}

## Permitindo acesso de {% data variables.product.prodname_github_apps %}

{% data reusables.identity-and-permissions.ip-allow-lists-githubapps-enterprise %}

## Habilitar endereços IP permitidos

{% data reusables.identity-and-permissions.about-enabling-allowed-ip-addresses %}

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.settings-tab %}
{% data reusables.enterprise-accounts.security-tab %}
1. Em "IP allow list" (Lista de permissões IP), selecione **Enable IP allow list** (Habilitar lista de permissões IP). ![Caixa de seleção para permitir endereços IP](/assets/images/help/security/enable-ip-allowlist-enterprise-checkbox.png)
4. Clique em **Salvar**.

## Editar endereços IP permitidos

{% data reusables.identity-and-permissions.about-editing-ip-allow-list-entries %}

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.settings-tab %}
{% data reusables.enterprise-accounts.security-tab %}
{% data reusables.identity-and-permissions.ip-allow-lists-edit-entry %}
{% data reusables.identity-and-permissions.ip-allow-lists-edit-ip %}
{% data reusables.identity-and-permissions.ip-allow-lists-edit-description %}
8. Clique em **Atualizar**.
{% data reusables.identity-and-permissions.check-ip-address %}

{% ifversion ip-allow-list-address-check %}
## Verificando se um endereço IP é permitido

{% data reusables.identity-and-permissions.about-checking-ip-address %}

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.settings-tab %}
{% data reusables.enterprise-accounts.security-tab %}
{% data reusables.identity-and-permissions.check-ip-address-step %}
{% endif %}

## Excluir endereços IP permitidos

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.settings-tab %}
{% data reusables.enterprise-accounts.security-tab %}
{% data reusables.identity-and-permissions.ip-allow-lists-delete-entry %}
{% data reusables.identity-and-permissions.ip-allow-lists-confirm-deletion %}

## Usar {% data variables.product.prodname_actions %} com uma lista endereços IP permitidos

{% data reusables.actions.ip-allow-list-self-hosted-runners %}
