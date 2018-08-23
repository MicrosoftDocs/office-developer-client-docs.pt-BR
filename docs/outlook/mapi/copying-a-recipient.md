---
title: Copiar um destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0105ac92c53424199685e76223e6d75792fb674e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566905"
---
# <a name="copying-a-recipient"></a>Copiar um destinatário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para copiar um ou mais destinatários de um contêiner para outra ou mesmo contêiner, verifique se o contêiner de destino é modificável. Contêineres que podem ser modificadas definir o sinalizador AB_MODIFIABLE em sua propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)).
  
Para copiar uma ou mais entradas em um recipiente modificável, chame o método de [IABContainer::CopyEntries](iabcontainer-copyentries.md) do contêiner de destino. Como copiar entradas do catálogo de endereços pode ser demorada, **CopyEntries** aceita quatro parâmetros de entrada: uma matriz de identificadores de entrada para uma bitmask dos sinalizadores, um identificador da janela, um indicador de progresso e as entradas a serem copiados. 
  
O indicador de janela alça e o progresso são usados pelo provedor de catálogo de endereços para mostrar o status da operação ao usuário. Se você deseja exibir o progresso, passar um identificador da janela para a janela pai do indicador de progresso no parâmetro _ulUIParam_ e não definir o sinalizador AB_NO_DIALOG no parâmetro _ulFlags_ . Se você tiver sua própria implementação de um indicador de progresso, passe um ponteiro para a implementação no parâmetro _lpProgress_ . Caso contrário, passe NULL. O provedor de catálogo de endereços usará a implementação de indicador de progresso MAPI. 
  
A bitmask dos sinalizadores indica se ou não deseja exibir um indicador de progresso e entrada como duplicada verificação devem ser tratados. Defina o sinalizador AB_NO_DIALOG para suprimir um indicador de progresso. Defina o sinalizador CREATE_CHECK_DUP_LOOSE para instruir o provedor de catálogo de endereços flexível Procurar duplicatas ou o sinalizador CREATE_CHECK_DUP_STRICT para verificação duplicados mais restrito. Definir o sinalizador CREATE_REPLACE para copiar entradas substituir as entradas existentes quando o provedor determina existirem duplicatas. 
  
Ao copiar em um contêiner de catálogo (PAB) particular de endereços, o provedor copia algumas ou todas as propriedades para cada entrada. Porque o MAPI não estabelece requisitos para provedores de implementar as operações de cópia de contêiner, você não pode fazer suposições sobre o número e o tipo de propriedades que são copiados com uma entrada de catálogo de endereços.
  

