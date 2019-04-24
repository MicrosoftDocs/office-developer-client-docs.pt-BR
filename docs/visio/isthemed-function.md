---
title: Função ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Retorna um valor Boolean que indica se uma forma tem um tema aplicado a ela.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357509"
---
# <a name="isthemed-function"></a>Função ISTHEMED

Retorna um valor Boolean que indica se uma forma tem um tema aplicado a ela. 
  
## <a name="version-information"></a>Informações sobre a versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **** Isthemeed ()
  
## <a name="return-value"></a>Valor de retorno

Booliano
  
## <a name="remarks"></a>Comentários

> [!NOTE]
> A **** função isthemes no Visio 2013 substitui a função **CELLISTHEMED** de versões anteriores do Visio. 
  
A **** função isthemes permite que você atribua partes apropriadas da formatação de um tema a uma forma, mas mantenha a capacidade de substituir outras partes da formatação do tema pela formatação aplicada manualmente. Se você reaplicar o tema subsequentemente, qualquer formatação manual será substituída e a forma assumirá toda a formatação do tema. 
  
 **** Isthemes é avaliado como true se a célula [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) na forma for maior que 0. Se essa célula for igual a 0, isTHEMEs será avaliada como FALSE. **** O tema do DocumentSheet e do PageSheet não afetará o valor da **** função isthemes usada em um ShapeSheet. Somente se a **** função isthemes aparecer no PageSheet o tema da página é importante. 
  
## <a name="example"></a>Exemplo

||||
|:-----|:-----|:-----|
|Cell  <br/> |Fórmula  <br/> |Resultado  <br/> |
|Fonte Char.  <br/> |IF (isTHEMEed (), THEMEVAL (), FONT ("Calibri"))  <br/> |Se a forma tiver um temas aplicada a ela, o texto da forma aceitará a formatação de fonte do tema. Se a forma não tiver temas, o texto da forma será formatado com a fonte "Calibri".  <br/> |
|LineColor  <br/> |SE (ISTHEMEED, RGB (255, 0, 0), RGB (0, 255, 0))  <br/> |Se a forma tiver um tema aplicada a ela, a cor da linha da forma será vermelha. Se a forma não tiver temas, a cor da linha da forma será verde.  <br/> |
   

