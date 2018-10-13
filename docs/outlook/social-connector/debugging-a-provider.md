---
title: Depurar um provedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Há várias maneiras de depurar um provedor de serviços do Outlook Social Connector (OSC):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386849"
---
# <a name="debugging-a-provider"></a>Depurar um provedor

Há várias maneiras de depurar um provedor de serviços do Outlook Social Connector (OSC): 
  
- Usando os comandos de depuração no componente da faixa de opções da interface de usuário do Office Fluent no Outlook ou o aplicativo de suporte ao do Office você pode fazer com que o OSC execute várias ações.
    
- Usando Fiddler para rastrear chamadas de API de e XML enviadas entre o seu provedor OSC e uma rede social
    
## <a name="debug-buttons"></a>Botões de depurar

A extensibilidade do provedor OSC fornece a capacidade de depuração de um provedor do OSC. Para depurar um provedor, crie um chave `DebugProviders` com o valor DWORD no registro do Windows na `SocialConnector` (como mostrado na linha seguinte) e configure o `DebugProviders` valor 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
Por padrão, o provedor de depuração de bugs está desativado. Se o valor `DebugProviders` não estiver presente, ou estiver presente e definir o valor de 0, a depuração do provedor estará desativada. 
  
Se o provedor de depuração de bugs estiver ativado, o OSC exibirá uma caixa de diálogo de alerta com informações detalhadas sobre erros, quando ocorrer um erro e validará qualquer XML de provedor OSC contra o esquema XML do provedor OSC. Com base no namespace especificado por uma cadeia de XML, um provedor de OSC que foi desenvolvido usando o OSC 1.0 é validado contra o esquema de arquivo OSC 1.0, OutlookSocialProvider.xsd. Um provedor de OSC desenvolvido usando OSC 1.1 ou posterior valida o arquivo de esquema OutlookSocialProvider_1.1.xsd. Quando você usa o valor`DebugProviders` o alerta de depuração é exibido para todos os provedores carregados em vez de um provedor específico. 
  
Para exibir os botões de depuração que podem te ajudar a deputar um provedor, crie um`ShowDebugButtons` com o valor DWORD no registro do Windows dentro da `SocialConnector` chave e configure o `ShowDebugButtons` valor 1. Para ocultar os botões da barra de comando depuração, defina o `ShowDebugButtons` valor como 0. 
  
Para aplicativos de clientes como o Office 2013 e Outlook 2010, os botões de depuração aparecem na guia **suplementos da faixa explorar de opções. Para o Outlook 2007 e o Outlook 2003, os botões de depuração aparecem na barra de comandos padrão da janela no Explorador do Outlook. 
  
A tabela a seguir descreve os botões de depurar.
  
|**Botões de depurar**|**Função**|
|:-----|:-----|
|Sincronizar contatos  <br/> |Faz com que o OSC peça ao provedor OSC somente contatos armazenados em cache.  <br/> |
|Sincronização do GAL  <br/> |Faz com que o OSC preencha dados da lista de endereços Global do Exchange para contatos do Outlook.  <br/> |
|Invalidar o Cache de categoria  <br/> |Faz com que o OSC recarregue a lista de categorias para cada loja quando o feed de atividades for atualizado.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler é uma ferramenta de depuração acima do fio para verificar chamadas de API enviadas para o seu provedor de rede social e XML enviados pela rede social para o seu provedor. Fiddler está disponível para download em[Fiddler Web Proxy de depuração](https://www.fiddler2.com/fiddler2/version.asp).
  
## <a name="see-also"></a>Confira também

- [Etapas rápidas para aprender a desenvolver um provedor](quick-steps-for-learning-to-develop-a-provider.md)  
- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md) 
- [Práticas recomendadas para o desenvolvimento de um provedor](best-practices-for-developing-a-provider.md)
- [Sequências de chamadas típicas de OSC](osc-typical-calling-sequences.md)  
- [Desenvolver um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Preparando um provedor de OSC para lançamento](getting-ready-to-release-an-osc-provider.md)

