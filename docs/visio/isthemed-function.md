---
title: Função ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Retorna um valor Boolean que indica se uma forma tem um tema aplicado a ela.
ms.openlocfilehash: 4311780d8686b5792e999c204ec182d23efb723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772138"
---
# <a name="isthemed-function"></a>Função ISTHEMED

Retorna um valor Boolean que indica se uma forma tem um tema aplicado a ela. 
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **ISTHEMED** ()
  
## <a name="return-value"></a>Valor retornado

Booliano
  
## <a name="remarks"></a>Comentários

> [!NOTE]
> A função **ISTHEMED** no Visio 2013 substitui a função **CELLISTHEMED** das versões anteriores do Visio. 
  
O **ISTHEMED** funcionar permite atribuir partes adequadas de formatação de um tema a uma forma, mas manter a capacidade de substituir a outras partes do tema formatação com a formatação aplicada manualmente. Se você subsequentemente reaplicar o tema, qualquer formatação manual será substituída e forma leva em toda a formatação do tema. 
  
 **ISTHEMED** é avaliada como TRUE se a célula [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) na forma for maior que 0. Se esta célula for igual a 0, **ISTHEMED** avalie como FALSE. O tema do DocumentSheet e PageSheet não afetará o valor da função **ISTHEMED** usado em um ShapeSheet. Somente se a função **ISTHEMED** aparecerá no PageSheet faz questão de tema da página. 
  
## <a name="example"></a>Exemplo

||||
|:-----|:-----|:-----|
|Célula  <br/> |Fórmula  <br/> |Resultado  <br/> |
|Char.Font  <br/> |IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))  <br/> |Se a forma tiver um com tema aplicado a ele, o texto da forma aceita a formatação do tema de fonte. Se a forma não estiver com temas, o texto da forma é formatado com a fonte "Calibri".  <br/> |
|LineColor  <br/> |IF (ISTHEMED, RGB (255, 0, 0), RGB (0, 255, 0))  <br/> |Se a forma tiver um com tema aplicado a ela, a cor da linha da forma é vermelho. Se a forma não estiver com temas, a cor da linha da forma é verde.  <br/> |
   

