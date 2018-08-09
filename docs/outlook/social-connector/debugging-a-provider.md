---
title: Depurar um provedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Há várias maneiras que você pode depurar um provedor do Outlook Social Connector (OSC):'
ms.openlocfilehash: ada439ca3b038ca9a0e849b47ff6a5f54e5016f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770829"
---
# <a name="debugging-a-provider"></a>Depurar um provedor

Há várias maneiras que você pode depurar um provedor do Outlook Social Connector (OSC): 
  
- Usando os comandos debug no componente da faixa de opções da interface de usuário Office Fluent no Outlook ou no aplicativo cliente do Office de suporte para fazer com que o OSC levar a várias ações.
    
- Usando o Fiddler para chamadas de API de rastreamento e XML enviadas entre uma rede social e seu provedor OSC
    
## <a name="debug-buttons"></a>Botões de depuração

A extensibilidade do provedor OSC oferece a capacidade de um provedor OSC de depuração. Para depurar um provedor, crie um `DebugProviders` valor do tipo DWORD no registro do Windows sob o `SocialConnector` principais (conforme mostrado na seguinte linha) e defina o `DebugProviders` valor como 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
Por padrão, o provedor de depuração está desativada. Se o `DebugProviders` valor não estiver presente, ou ele está presente e definido com um valor 0, o provedor de depuração está desativado. 
  
Se o provedor de depuração está ativado, o OSC exibe uma caixa de diálogo alerta com informações de erro verbose quando ocorre um erro e valida qualquer provedor OSC XML em relação ao esquema XML de provedor do OSC. Um provedor OSC desenvolvido usando OSC 1.0 com base no namespace especificado para uma sequência de caracteres XML, é validado contra o arquivo de esquema OSC 1.0, OutlookSocialProvider.xsd. Um provedor OSC desenvolvidos usando OSC 1.1 ou posterior é validado contra o arquivo de esquema, OutlookSocialProvider_1.1.xsd. Quando você usa o `DebugProviders` valor, o alerta de depuração aparece para todos carregados provedores em vez de um provedor específico. 
  
Para exibir os botões de depuração que podem ajudá-lo um provedor de depuração, crie um `ShowDebugButtons` valor do tipo DWORD no registro do Windows sob o `SocialConnector` principais e definir o `ShowDebugButtons` valor como 1. Para ocultar os botões de barra de comandos de depuração, defina o `ShowDebugButtons` valor como 0. 
  
Para o Outlook 2010 e aplicativos de cliente desde o Office 2013, os botões de depuração aparecem na guia **suplementos** da faixa de opções do explorer. Para o Outlook 2007 e Outlook 2003, os botões de depuração aparecem na barra de comandos padrão da janela do explorer do Outlook. 
  
A tabela a seguir descreve os botões de depuração.
  
|**Botão de depuração**|**Function**|
|:-----|:-----|
|Sincronizar contatos  <br/> |Faz com que o OSC pedir o provedor do OSC apenas os contatos em cache.  <br/> |
|Sincronização da GAL  <br/> |Faz com que o OSC preencher dados da lista de endereços Global do Exchange para contatos do Outlook.  <br/> |
|Invalidar o Cache de categoria  <br/> |Faz com que o OSC recarregar a lista de categorias para cada repositório quando o feed de atividade for atualizado.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler é uma ferramenta de depuração do over-durante a transmissão para verificar a chamadas à API enviadas do seu provedor para a rede social e XML enviadas pela rede social para seu provedor. Fiddler está disponível para download no [Proxy de depuração da Web Fiddler](http://www.fiddler2.com/fiddler2/version.asp).
  
## <a name="see-also"></a>Confira também

- [Etapas rápidas de aprendizado para desenvolver um provedor](quick-steps-for-learning-to-develop-a-provider.md)  
- [Sincronização de amigos e atividades](synchronizing-friends-and-activities.md) 
- [Práticas recomendadas para o desenvolvimento de um provedor](best-practices-for-developing-a-provider.md)
- [Sequências de chamadas comuns do OSC](osc-typical-calling-sequences.md)  
- [Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md)  
- [Preparando-se para o lançamento de um provedor OSC](getting-ready-to-release-an-osc-provider.md)

