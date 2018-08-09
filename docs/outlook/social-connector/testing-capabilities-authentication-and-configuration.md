---
title: Testar recursos, autenticação e configuração
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: Este tópico descreve os testes para obtenção de recursos e cenários em torno Configurando uma conta e autenticação de um usuário para uma rede social.
ms.openlocfilehash: ac294291e2226dbb73f822b2a641fe2bf67ce5eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770956"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Testar recursos, autenticação e configuração

Este tópico descreve os testes para obtenção de recursos e cenários em torno Configurando uma conta e autenticação de um usuário para uma rede social.
  
## <a name="getting-capabilities"></a>Recursos de Introdução

Um provedor do Outlook Social Connector (OSC) implementa [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)e as chamadas OSC **GetCapabilities** para obter a funcionalidade suportada pelo provedor. Os recursos que o provedor oferece suporte para a sua rede social devem ser conhecidos no ponto de implementação e não devem depender de uma chamada para a rede social em tempo real. Por exemplo, os usuários do Outlook podem iniciar o Outlook offline e **GetCapabilities** não pode depender da conectividade de rede no momento quando o Outlook for iniciado. 
  
Ao testar o provedor, você deve verificar se o parâmetro de sequência de _resultados_ retornado pelo **GetCapabilities** está em conformidade com o elemento de **recursos** conforme definido pelo esquema XML de provedor do OSC. Para obter mais informações, consulte [Elementos XML de recursos](capabilities-xml-elements.md).
  
## <a name="configuring-an-account"></a>Configurando uma conta

Quando o OSC configura uma conta, você deve verificar se o ícone de redes sociais e o nome são exibidas e se os hiperlinks criar conta e senha esqueceu são exibidas na caixa de diálogo de configuração de conta, conforme especificado pelo provedor.
  
### <a name="social-network-icon-and-name"></a>Nome e o ícone de redes sociais

Depois de obter recursos, o OSC poderá continuar a fazer o ícone e o nome para a rede social chamando [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) e [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md). Execute os seguintes testes para verificar que essas chamadas de método bem-sucedida.
  
|**Item de teste**|**Comportamento esperado**|
|:-----|:-----|
|Ícone de redes sociais  <br/> | O ícone de rede social é exibido corretamente nos seguintes locais no OSC:  <br/>  Na caixa de diálogo OSC para **Contas de rede Social**.  <br/>  No menu suspenso quando você tentar adicionar uma pessoa como um amigo.  <br/>  No crachá quando seguindo um amigo.  <br/> <br/>**Observação**: você pode acessar a caixa de diálogo para **Contas de rede Social** clicando na guia **Exibir** , no Outlook, no **Painel pessoas** grupo, clicando em **Painel de pessoas**e, em seguida, clicando em **Configurações de conta**.           |
|Nome de rede social  <br/> | O nome de rede social é exibido corretamente nos seguintes locais no OSC:  <br/>  Na caixa de diálogo OSC para **Contas de rede Social**.  <br/>  No menu suspenso quando você tentar adicionar uma pessoa como um amigo.  <br/>  Como o título da caixa de diálogo senha quando você tentar alterar a senha existente.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Mostrando hiperlinks na caixa de diálogo de configuração

Depois de chamar **ISocialProvider::GetCapabilities**, o OSC usa o valor do elemento **hideHyperlinks** no parâmetro _resultados_ para determinar se deseja ocultar ou exibir o **clique aqui para criar uma conta** e **Esqueceu sua senha?** hiperlinks na caixa de diálogo de configuração de conta. Verifique se se **hideHyperlinks** for **false**, a configuração da conta exibe essas URLs.
  
### <a name="support-to-create-account"></a>Suporte para criar conta

Verifique se o parâmetro de _resultados_ na chamada de método **ISocialProvider::GetCapabilities** tem o elemento **hideHyperlinks** definida como **false** e o elemento **createAccountUrl** definido como **true**, clicando na URL Abre a página no navegador da web padrão.
  
### <a name="support-for-forgotten-password"></a>Suporte para recuperação de senha

Verifique se o parâmetro de _resultados_ na chamada de método **ISocialProvider::GetCapabilities** tem o elemento **hideHyperlinks** definida como **false** e o elemento **forgotPasswordUrl** definido como **true**, clicando na URL Abre a página no navegador da web padrão.
  
## <a name="authenticating-users"></a>Autenticação de usuários

Teste para os seguintes cenários independentemente se o seu provedor OSC oferece suporte à autenticação básica ou autenticação baseada em formulários.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|Fazendo logon pela primeira vez.  <br/> |O usuário pode fazer logon com êxito à rede social.  <br/> |
|Logon com uma senha formada por uma variedade de caracteres, incluindo pontuação e caracteres Unicode.  <br/> |O usuário pode fazer logon com êxito à rede social, independente do tipo de caracteres usados na senha.  <br/> |
|A caixa de diálogo **Contas de rede Social** exibindo o nome de usuário ou a ID.  <br/> |Depois que o usuário tem com êxito conectado à rede, a caixa de diálogo do OSC para **Contas de rede Social** exibe o nome do usuário conectado ou o ID.  <br/> |
|A autenticação falhará.  <br/> |O OSC exibe o erro de **nome de usuário inválido ou a senha**.  <br/> |
|Não é possível conectar-se à rede social.  <br/> |O OSC exibe o erro no **servidor não pode ser encontrado**.  <br/> |
|Ser capaz de recuperar itens.  <br/> |Depois que o usuário autenticado, todas as atividades devem ser permitidas. Não há nenhum erro Obtendo dados ou atividades de amigos dos.  <br/> |
|Fazer logon na rede de social após a reinicialização do Outlook.  <br/> |Se o provedor do OSC permitir o armazenamento em cache da senha, depois que o usuário autenticado na primeira vez, o usuário não é subsequentemente solicitado credenciais sempre que o OSC tenta obter dados a partir da rede social.  <br/> |
   
Além disso, se seu provedor OSC suporta a autenticação baseada em formulários, teste para o seguinte cenário.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|O OSC obtendo uma URL para um formulário para o usuário fazer logon de chamar [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md).  <br/> |O OSC abre a URL no navegador de padrão do usuário e a página da Web permite que o usuário insira credenciais para fazer logon na rede social.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Elementos XML de recursos](capabilities-xml-elements.md)  
- [Autenticação básica](basic-authentication.md) 
- [Autenticação baseada em formulários](forms-based-authentication.md)
- [Preparando-se para o lançamento de um provedor OSC](getting-ready-to-release-an-osc-provider.md)

