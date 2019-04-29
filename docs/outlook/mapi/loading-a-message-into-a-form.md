---
title: Carregar uma mensagem em um formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: afecd3b334dd2cf7b2953916872982e6459a8434
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412412"
---
# <a name="loading-a-message-into-a-form"></a>Carregar uma mensagem em um formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para carregar uma mensagem existente em um formulário usando um servidor de formulário, use uma das estratégias a seguir.
  
- Chame [IMAPISession::P repareform](imapisession-prepareform.md) para criar um token e, em seguida, [IMAPISession:: conform](imapisession-showform.md) para exibir o formulário. 
    
- Chamar [IMAPIFormMgr:: loadform](imapiformmgr-loadform.md). 
    
O uso da estratégia **PrepareForm** e de IsForm é comparativamente fácil, mas resulta em formulários restritos com relação ao cliente. **** Isso ocorre porque a chamada para o **formulário** exibir não retorna até que o formulário seja encerrado. Se você precisar lidar com formulários de forma assíncrona, não use essa estratégia. 
  
O uso **** da estratégia loadform é mais difícil porque o método requer vários parâmetros. Esses parâmetros instruem o gerente de formulário a iniciar o servidor de formulário adequado no contexto apropriado e a exibir a mensagem adequada. Se o servidor de formulário já estiver sendo executado, o Gerenciador de formulários carregará a mensagem no servidor de formulário sem iniciar uma nova instância do servidor de formulário. 
  
Para especificar qual servidor de formulário iniciar, passe a classe de mensagem manipulada pelo servidor de destino no conteúdo do parâmetro _lpszMessageClass_ . A classe de mensagem apropriada pode ser determinada recuperando a propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) da mensagem a ser carregada. Às vezes, não há servidor de formulário para a classe de mensagem especificada, somente um servidor de formulário que manipula mensagens pertencentes à superclasse da mensagem. Se você preferir que a mensagem seja carregada apenas por um servidor de formulário especificamente destinado a lidar com mensagens dessa classe, defina o sinalizador MAPIFORM_EXACTMATCH na **** chamada loadform. Para obter mais informações, consulte [MAPI Message classes](mapi-message-classes.md).
  
 **Loadform** também requer um ponteiro para o site de mensagens do seu visualizador e o contexto de exibição e o valor da **PR_MSG_STATUS** da mensagem de destino ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) e **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) Propriedades.
  

