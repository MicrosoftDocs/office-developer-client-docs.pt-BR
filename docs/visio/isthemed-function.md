---
title: Função ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Retorna um valor Boolean indicando se uma forma tem um tema aplicado a ela.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418117"
---
# <a name="isthemed-function"></a>Função ISTHEMED

Retorna um valor Boolean indicando se uma forma tem um tema aplicado a ela. 
  
## <a name="version-information"></a>Informações sobre a versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **ISTHEMED**()
  
## <a name="return-value"></a>Valor de retorno

Booliano
  
## <a name="remarks"></a>Comentários

> [!NOTE]
> A **função ISTHEMED** no Visio 2013 substitui a função **CELLISTHEMED** de versões anteriores do Visio. 
  
A **função ISTHEMED** permite atribuir partes apropriadas da formatação de um tema a uma forma, mas mantém a capacidade de substituir outras partes da formatação do tema pela formatação aplicada manualmente. Se você reaplicar posteriormente o tema, qualquer formatação manual será substituído e a forma assumirá toda a formatação do tema. 
  
 **ISTHEMED** avalia como TRUE se a [célula ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) na forma for maior que 0. Se essa célula for igual a 0, **ISTHEMED** será avaliada como FALSE. O tema da DocumentSheet e pageSheet não afetará o valor da função **ISTHEMED** usada em um ShapeSheet. Somente se a **função ISTHEMED** aparecer no PageSheet, o tema da página será importante. 
  
## <a name="example"></a>Exemplo

||||
|:-----|:-----|:-----|
|Cell  <br/> |Fórmula  <br/> |Resultado  <br/> |
|Char.Font  <br/> |IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))  <br/> |Se a forma tiver um tema aplicado a ela, o texto da forma aceitará a formatação da fonte do tema. Se a forma não tiver temas, o texto da forma será formatado com a fonte "Calibri".  <br/> |
|LineColor  <br/> |IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))  <br/> |Se a forma tiver um temas aplicado a ela, a cor da linha da forma será vermelho. Se a forma não tiver temas, a cor da linha da forma será verde.  <br/> |
   

