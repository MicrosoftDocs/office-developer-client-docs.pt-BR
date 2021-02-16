---
title: Testar recursos, autenticação e configuração
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: Este tópico descreve testes para obter recursos e cenários relacionados à configuração de uma conta e autenticação de um usuário para uma rede social.
ms.openlocfilehash: 218d5c564dd18e1e72820e31079011e6bb81a33c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423500"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Testar recursos, autenticação e configuração

Este tópico descreve testes para obter recursos e cenários relacionados à configuração de uma conta e autenticação de um usuário para uma rede social.
  
## <a name="getting-capabilities"></a>Obter recursos

Um provedor do Outlook Social Connector (OSC) implementa [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)e o OSC chama **GetCapabilities** para obter a funcionalidade suportada pelo provedor. Os recursos que seu provedor suporta para sua rede social devem ser conhecidos no ponto de implementação e não devem depender de uma chamada para a rede social em tempo real. Por exemplo, os usuários do Outlook podem iniciar o Outlook offline, e **o GetCapabilities** não pode depender da conectividade de rede no momento em que o Outlook é iniciado. 
  
Ao testar o provedor, você  deve verificar se o parâmetro de cadeia de caracteres de resultados retornado por **GetCapabilities** está em conformidade com o elemento **capabilities** conforme definido pelo esquema XML do provedor OSC. Para obter mais informações, consulte [Elementos XML de recursos.](capabilities-xml-elements.md)
  
## <a name="configuring-an-account"></a>Configurando uma conta

Quando o OSC configura uma conta, você deve verificar se o ícone e o nome da rede social são exibidos e se os hiperlinks criar conta e esqueceu-senha aparecem na caixa de diálogo de configuração da conta, conforme especificado pelo provedor.
  
### <a name="social-network-icon-and-name"></a>Nome e ícone de rede social

Depois de obter recursos, o OSC pode continuar a obter o ícone e o nome da rede social chamando [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) e [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md). Faça os seguintes testes para verificar se essas chamadas de método foram bem-sucedidas.
  
|**Item a ser testado**|**Comportamento esperado**|
|:-----|:-----|
|Ícone de rede social  <br/> | O ícone de rede social é exibido corretamente nos seguintes locais no OSC:  <br/>  Na caixa de diálogo OSC para Contas **de Rede Social.**  <br/>  No menu suspenso quando você tenta adicionar uma pessoa como um amigo.  <br/>  No selo ao seguir um amigo.  <br/> <br/>**OBSERVAÇÃO:** você pode acessar  a caixa de diálogo para Contas de  Redes Sociais clicando na guia Exibir no Outlook, no grupo Painel de Pessoas, clicando no Painel de Pessoas e em Configurações da **Conta.**            |
|Nome da rede social  <br/> | O nome da rede social é exibido corretamente nos seguintes locais no OSC:  <br/>  Na caixa de diálogo OSC para Contas **de Rede Social.**  <br/>  No menu suspenso quando você tenta adicionar uma pessoa como um amigo.  <br/>  Como o título da caixa de diálogo de senha quando você tenta alterar a senha existente.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Mostrando hiperlinks na caixa de diálogo de configuração

Depois de chamar **ISocialProvider::GetCapabilities**, o OSC usa o valor  do elemento **hideHyperlinks** no parâmetro de resultados para determinar se deve ocultar ou exibir o clique aqui para criar uma conta e esqueceu sua **senha?** Hiperlinks na caixa de diálogo de configuração da conta.  Verifique se **hideHyperlinks** é **falso**, a configuração da conta exibe essas URLs.
  
### <a name="support-to-create-account"></a>Suporte para criar conta

Verifique se  se o parâmetro de resultados da chamada do método **ISocialProvider::GetCapabilities** tiver o elemento **hideHyperlinks** definido como **falso** e o elemento **createAccountUrl** definido como **true**, clicar na URL abrirá a página no navegador da Web padrão.
  
### <a name="support-for-forgotten-password"></a>Suporte para senha esquecida

Verifique se  se o parâmetro de resultados da chamada do método **ISocialProvider::GetCapabilities** tiver o elemento **hideHyperlinks** definido como **false** e o elemento **forgotPasswordUrl** definido como **true**, clicar na URL abrirá a página no navegador da Web padrão.
  
## <a name="authenticating-users"></a>Autenticação de usuários

Teste os seguintes cenários, independentemente de seu provedor OSC suportar autenticação básica ou autenticação baseada em formulários.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|Logor pela primeira vez.  <br/> |O usuário pode fazer logoff com êxito na rede social.  <br/> |
|Fazer logon com uma senha com uma variedade de caracteres, incluindo pontuação e caracteres Unicode.  <br/> |O usuário pode fazer logoff com êxito na rede social, independentemente do tipo de caracteres usados na senha.  <br/> |
|A caixa de diálogo para **Contas de Redes Sociais** exibindo o nome de usuário ou ID.  <br/> |Depois que o usuário tiver se conectado com êxito à rede, a caixa de diálogo do OSC para Contas de Rede **Social** exibirá o ID ou o nome de usuário conectado.  <br/> |
|A autenticação falha.  <br/> |O OSC exibe o erro Nome **de usuário ou senha inválido.**  <br/> |
|Não é possível se conectar à rede social.  <br/> |The OSC displays the error **Server cannot be found**.  <br/> |
|Ser capaz de recuperar itens.  <br/> |Depois que o usuário autenticar, todas as atividades deverão ser permitidas. Não há erros ao obter dados ou atividades de amigos.  <br/> |
|Logor na rede social após reiniciar o Outlook.  <br/> |Se o provedor OSC permitir o armazenamento em cache da senha, depois que o usuário autenticar pela primeira vez, o usuário não será solicitado a obter credenciais subsequentemente sempre que o OSC tentar obter dados da rede social.  <br/> |
   
Além disso, se o provedor do OSC oferece suporte à autenticação baseada em formulários, teste também o cenário a seguir.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|The OSC getting a URL to a form for the user to log on from calling [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md).  <br/> |O OSC abre a URL no navegador padrão do usuário, e a página da Web permite que o usuário insira credenciais para fazer logon na rede social.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Elementos XML de recursos](capabilities-xml-elements.md)  
- [Autenticação básica](basic-authentication.md) 
- [Autenticação baseada em formulários](forms-based-authentication.md)
- [Preparar um provedor de OSC para lançamento](getting-ready-to-release-an-osc-provider.md)

