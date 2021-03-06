---
title: Célula LockFromGroupFormat (Seção Proteção)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426055"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>Célula LockFromGroupFormat (Seção Proteção)

Impede que as alterações de formato em uma forma de grupo seja propagada para suas sub formas, enquanto ainda permite que os usuários forndem sub formas selecionadas diretamente. 
  
O valor da célula LockFromGroupFormat corresponde à configuração da caixa de seleção **De formatação de grupo** na caixa de diálogo **Proteção**. 
  
Para referir-se à célula LockFromGroupFormat pelo nome de outra fórmula, ou a partir de um programa, usando a propriedade **CellsU**, utilize:

 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LockFromGroupFormat  <br/> |
   
Para referir-se à célula LockFromGroupFormat pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowLock** <br/> |
|Índice de célula:  <br/> |**visLockFromGroupFormat** <br/> |
   
O valor padrão da célula é 0 (False).
  

