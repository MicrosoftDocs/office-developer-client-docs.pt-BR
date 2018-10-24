---
title: Vis�o geral da programa��o MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: 'Última modificação: 25 de julho de 2012'
ms.openlocfilehash: bd9cdd9119f94e1f7684be34e1b4ef6fb40ab2bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576502"
---
# <a name="mapi-programming-overview"></a>Vis�o geral da programa��o MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Esta referência Microsoft Outlook Messaging API (MAPI) foi elaborada para C e com uma variedade de desenvolvedores do C++ precisa e experiência com mensagens. Para os desenvolvedores que desejam usar MAPI para incrementar seus aplicativos que têm recursos de mensagens, nenhum conhecimento de pré-requisito específico é necessário. Você precisa de um plano de fundo em mensagens e o modelo COM (Component Object) usar MAPI para criar aplicativos de larga escala do grupo de trabalho ou drivers de serviços do sistema de mensagens especializados.
  
Antes de iniciar o trabalho de desenvolvimento, você deve considerar as seguintes informações sobre como usar o MAPI, o processo de logon e como perfis e serviços de mensagem sejam criados e configurados.
  
O programa Interface MAPI (Messaging Application) é um amplo conjunto de funções que os desenvolvedores podem usar para criar aplicativos habilitados para email. A biblioteca de função completa é conhecida como MAPI. MAPI permite controle total sobre o sistema de mensagens no computador cliente, criação e gerenciamento de mensagens, gerenciamento da caixa de correio do cliente, provedores de serviços e assim por diante.
  
> [!NOTE]
> MAPI estendido é o mesmo MAPI e simplesmente é conhecido como MAPI na documentação de MAPI. 
  
 **MAPI simples**
  
MAPI simples fornece um conjunto de funções que permite que você adicione um nível básico de funcionalidade aos aplicativos do Microsoft baseado no Windows de mensagens.
  
> [!IMPORTANT]
> A função de MAPI simples MAPISendMail é compatível com o Microsoft Outlook 2013 e o Microsoft Outlook 2010. Outras funções de MAPI simples foram preteridas no Windows. 
  

