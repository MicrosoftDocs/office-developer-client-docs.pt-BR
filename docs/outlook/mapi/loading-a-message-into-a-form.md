---
title: Carregar uma mensagem em um formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6e65311187ba96abde31a4779ebba371b3d02084
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576495"
---
# <a name="loading-a-message-into-a-form"></a>Carregar uma mensagem em um formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para carregar uma mensagem existente em um formulário usando um servidor de formulário, use uma das seguintes estratégias.
  
- [PrepareForm](imapisession-prepareform.md) para criar um token de chamada e, em seguida, [IMAPISession:: ShowForm](imapisession-showform.md) para exibir o formulário. 
    
- Chame [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md). 
    
Usando a estratégia de **PrepareForm** e **ShowForm** é relativamente fácil, mas ele implica formulários que são modais em relação ao seu cliente. Isso ocorre porque a chamada para **ShowForm** não retorna até que o formulário foi encerrado. Se você precisar manipular formulários de forma assíncrona, não use essa estratégia. 
  
Usando a estratégia de **LoadForm** é mais difícil, pois o método requer vários parâmetros. Esses parâmetros instruem o Gerenciador de formulário para iniciar o servidor de forma adequada no contexto adequado e exibir a mensagem apropriada. Se o servidor de formulário já estiver em execução, o gerente de formulário carrega a mensagem para o servidor de formulário sem lançar uma nova instância do servidor do formulário. 
  
Para especificar qual servidor formulário início, passe a classe de mensagem manipulada pelo servidor de destino no conteúdo do parâmetro _lpszMessageClass_ . A classe de mensagem apropriada pode ser determinada pela Recuperando a propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) da mensagem a ser carregada. Em alguns casos, não há nenhum servidor de formulário para a classe de mensagem especificada, somente um servidor de formulário que trata as mensagens que pertencem a superclasse da mensagem. Se você preferir que a mensagem ser carregado somente por um servidor de formulário especificamente desenvolvido para lidar com as mensagens de classe, defina o sinalizador MAPIFORM_EXACTMATCH na chamada **LoadForm** . Para obter mais informações, consulte [Classes de mensagem MAPI](mapi-message-classes.md).
  
 **LoadForm** também requer um ponteiro para o site de mensagem do seu visualizador e contexto de modo de exibição e o valor para a mensagem de destino **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) e o **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) Propriedades.
  

