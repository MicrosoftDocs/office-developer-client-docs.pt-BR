---
title: Copiando um destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3a4fb1a3f76481bf1960c251a33911b871a8791c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419083"
---
# <a name="copying-a-recipient"></a>Copiando um destinatário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para copiar um ou mais destinatários de um contêiner para outro ou para o mesmo contêiner, primeiro verifique se o contêiner de destino é modificável. Os contêineres que são modificáveis configuram o sinalizador AB_MODIFIABLE na propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)).
  
Para copiar uma ou mais entradas para um contêiner modificável, chame o método [IABContainer::CopyEntries do](iabcontainer-copyentries.md) contêiner de destino. Como a cópia de entradas do livro de endereços pode ser demorada, **CopyEntries** aceita quatro parâmetros de entrada: uma matriz de identificadores de entrada para as entradas a serem copiadas, um identificador de janela, um indicador de progresso e uma bitmask de sinalizadores. 
  
O indicador de progresso e o indicador de janela são usados pelo provedor de agendas para mostrar o status da operação para o usuário. Se você quiser exibir o progresso, passe uma alça de janela para a janela pai do indicador de progresso no parâmetro _ulUIParam_ e não defina o sinalizador AB_NO_DIALOG no parâmetro _ulFlags._ Se você tiver sua própria implementação de um indicador de progresso, passe um ponteiro para a implementação no _parâmetro lpProgress._ Caso não seja, passe NULL. O provedor de agendas usará a implementação do indicador de progresso MAPI. 
  
A máscara de bits de sinalizadores indica se você deseja ou não exibir um indicador de progresso e como a verificação de entrada duplicada deve ser tratada. De definida a AB_NO_DIALOG sinalizador para suprimir um indicador de progresso. De configurar o CREATE_CHECK_DUP_LOOSE para instruir o provedor de agendas a verificar se há duplicatas ou o sinalizador CREATE_CHECK_DUP_STRICT para verificação duplicada mais estrita. Definir o CREATE_REPLACE sinalizador para que as entradas copiadas substituam as entradas existentes quando o provedor determinar que há duplicatas. 
  
Ao copiar para um contêiner de pab (lista de endereços pessoal), o provedor copia algumas ou todas as propriedades para cada entrada. Como o MAPI não estabelece requisitos para provedores que implementam operações de cópia de contêiner, você não pode fazer suposições sobre o número e o tipo de propriedades que são copiadas com uma entrada do livro de endereços.
  

