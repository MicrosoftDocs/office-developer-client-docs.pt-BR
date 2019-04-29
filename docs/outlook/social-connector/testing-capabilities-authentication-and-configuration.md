---
title: Testar recursos, autenticação e configuração
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: Este tópico descreve os testes para obter recursos e cenários sobre como configurar uma conta e autenticar um usuário para uma rede social.
ms.openlocfilehash: 218d5c564dd18e1e72820e31079011e6bb81a33c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423500"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Testar recursos, autenticação e configuração

Este tópico descreve os testes para obter recursos e cenários sobre como configurar uma conta e autenticar um usuário para uma rede social.
  
## <a name="getting-capabilities"></a>Obtendo recursos

Um provedor do Outlook Social Connector (OSC) implementa [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md)e o OSC chama **GetCapabilities** para obter a funcionalidade suportada pelo provedor. Os recursos que seu provedor oferece suporte à sua rede social devem ser conhecidos no ponto de implementação e não devem depender de uma chamada para a rede social em tempo real. Por exemplo, os usuários do Outlook podem iniciar o Outlook **** offline e o GetCapabilities não pode depender da conectividade de rede no momento em que o Outlook é iniciado. 
  
Ao testar o provedor, você deve verificar se o parâmetro de cadeia de caracteres de _resultados_ retornado por GetCapabilities está em conformidade com o elemento **Capabilities** , conforme definido pelo esquema XML do provedor do OSC. **** Para obter mais informações, consulte [Capabilities XML Elements](capabilities-xml-elements.md).
  
## <a name="configuring-an-account"></a>ConFigurando uma conta

Quando o OSC configura uma conta, você deve verificar se o ícone e o nome da rede social são exibidos e se os hiperlinks de criação e esqueci-password aparecem na caixa de diálogo de configuração da conta conforme especificado pelo provedor.
  
### <a name="social-network-icon-and-name"></a>Ícone e nome da rede social

Depois de obter recursos, o OSC pode prosseguir para obter o ícone e o nome da rede social chamando [ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) e [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md). Execute os testes a seguir para verificar se essas chamadas de método foram bem-sucedidas.
  
|**Item a ser testado**|**Comportamento esperado**|
|:-----|:-----|
|Ícone de rede social  <br/> | O ícone de rede social é exibido corretamente nos seguintes locais no OSC:  <br/>  Na caixa de diálogo OSC para **contas de rede social**.  <br/>  No menu suspenso ao tentar adicionar uma pessoa como um amigo.  <br/>  No emblema ao seguir um amigo.  <br/> <br/>**Observação**: você pode acessar a caixa de diálogo para **contas de rede social** clicando na guia **Exibir** no Outlook, no grupo **painel de pessoas** , clicando em painel de **pessoas**e, em seguida, clicando em configurações de **conta**.           |
|Nome da rede social  <br/> | O nome da rede social é exibido corretamente nos seguintes locais no OSC:  <br/>  Na caixa de diálogo OSC para **contas de rede social**.  <br/>  No menu suspenso ao tentar adicionar uma pessoa como um amigo.  <br/>  Como o título da caixa de diálogo de senha quando você tenta alterar a senha existente.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Mostrando hiperlinks na caixa de diálogo de configuração

Após chamar **ISocialProvider:: GetCapabilities**, o OSC usa o valor do elemento **hideHyperlinks** no parâmetro _Results_ para determinar se deseja ocultar ou exibir o **clique aqui para criar uma conta** e esqueceu-se do **seu senha?** hiperlinks na caixa de diálogo de configuração da conta. Verifique se **hideHyperlinks** é **false**, se a configuração da conta exibe essas URLs.
  
### <a name="support-to-create-account"></a>Suporte para criar conta

Verifique se o parâmetro _Results_ da chamada do método **ISocialProvider:: GetCapabilities** tem o elemento **hideHyperlinks** definido como **false** e o elemento **createAccountUrl** definido como **true**, clicando na URL Abre a página no navegador da Web padrão.
  
### <a name="support-for-forgotten-password"></a>Suporte para senha esquecida

Verifique se o parâmetro _Results_ da chamada do método **ISocialProvider:: GetCapabilities** tem o elemento **hideHyperlinks** definido como **false** e o elemento **forgotPasswordUrl** definido como **true**, clicando na URL Abre a página no navegador da Web padrão.
  
## <a name="authenticating-users"></a>Autenticação de usuários

Teste os cenários a seguir independentemente de seu provedor do OSC oferecer suporte à autenticação básica ou à autenticação baseada em formulários.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|Fazer logon pela primeira vez.  <br/> |O usuário pode fazer logon na rede social com êxito.  <br/> |
|Fazer logon com uma senha composta por uma variedade de caracteres, incluindo pontuação e caracteres Unicode.  <br/> |O usuário pode fazer logon na rede social com êxito, independente do tipo de caracteres usado na senha.  <br/> |
|A caixa de diálogo para **contas de rede social** exibindo o nome de usuário ou ID.  <br/> |Depois que o usuário tiver feito logon com êxito na rede, a caixa de diálogo do OSC para **contas de rede social** exibirá o nome do usuário conectado ou a ID.  <br/> |
|A autenticação falha.  <br/> |O OSC exibe o **nome de usuário ou senha inválido**do erro.  <br/> |
|Não é possível conectar-se à rede social.  <br/> |O OSC exibe o servidor de erro **não pode ser encontrado**.  <br/> |
|Ser capaz de recuperar itens.  <br/> |Após a autenticação do usuário, todas as atividades devem ser permitidas. Não há erros para obter dados ou atividades dos amigos.  <br/> |
|Fazer logon na rede social após reiniciar o Outlook.  <br/> |Se o provedor do OSC permitir o cache da senha, após o usuário ter sido autenticado pela primeira vez, o usuário não será solicitado a fornecer as credenciais sempre que o OSC tentar obter dados da rede social.  <br/> |
   
Além disso, se o provedor OSC oferecer suporte à autenticação baseada em formulários, teste o cenário a seguir também.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|O OSC obtendo uma URL para um formulário para que o usuário faça logon de chamar [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md).  <br/> |O OSC abre a URL no navegador padrão do usuário e a página da Web permite que o usuário insira as credenciais para fazer logon na rede social.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Elementos XML de recursos](capabilities-xml-elements.md)  
- [Autenticação básica](basic-authentication.md) 
- [Autenticação baseada em formulários](forms-based-authentication.md)
- [Preparar um provedor de OSC para lançamento](getting-ready-to-release-an-osc-provider.md)

