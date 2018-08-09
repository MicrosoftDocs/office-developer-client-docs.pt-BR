---
title: Célula LockFromGroupFormat (Seção Proteção)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 95633ab7a4127564fef65062bcf328d4364ebd86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772260"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>Célula LockFromGroupFormat (Seção Protection)

Blocos de formato alterações a uma forma de grupo sejam propagadas para suas subformas enquanto ainda permite que os usuários formatar as formas selecionadas sub-recurso diretamente. 
  
O valor da célula LockFromGroupFormat corresponde à configuração da caixa de seleção **De formatação de grupo** na caixa de diálogo **Proteção**. 
  
Para referir-se à célula LockFromGroupFormat pelo nome de outra fórmula, ou a partir de um programa, usando a propriedade **CellsU**, utilize:

 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LockFromGroupFormat  <br/> |
   
Para referir-se à célula LockFromGroupFormat pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:

 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowLock** <br/> |
|Índice da célula:  <br/> |**visLockFromGroupFormat** <br/> |
   
O valor padrão da célula é 0 (False).
  

