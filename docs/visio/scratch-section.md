---
title: Seção Scratch
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
localization_priority: Normal
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
description: Uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.
ms.openlocfilehash: 16f0bac8f139c0b03d7826ac377a964d15296dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772845"
---
# <a name="scratch-section"></a>Seção Scratch

Uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.
  
## <a name="remarks"></a>Comentários

É possível adicionar essa seção usando a caixa de diálogo **Inserir Seção**. Clique com o botão direito do mouse na janela do ShapeSheet e clique em **Inserir Seção**.
  
A seção **Scratch** geralmente é usada para isolar cálculos complexos repetidos. Se a solução tiver um objetivo bem definido, é mais sensato usar uma célula na seção **User-Defined Cells** para manter a clareza, pois as células de usuário podem ser nomeadas. 
  
Células na seção **Scratch** usem unidades de duas maneiras diferentes. Células X e Y usam unidades de desenho; Um até células de D não usam unidades. (No jargão dos programadores C, células X e Y são "digitadas" e células de À D são "anuladas".) As células **Scratch X** e **Y de Scratch** geralmente são usadas para derivar as coordenadas *x* e *y* , como **PinX** e **PinY**ou as células X e Y encontradas em uma célula da seção **Geometry** . Células de que à D pode exibir qualquer unidade que você especificar transitórias. 
  
Outra diferença é a maneira que essas células armazenam valores de ponto. Um ponto no Visio é um pacote de dados único para uma coordenada ( *x, y*). Quando uma fórmula retorna um valor de ponto, esse valor será interpretado em uma destas três formas, dependendo da célula ShapeSheet que a fórmula é no. As células que se relacionam com *x* -coordenadas (por exemplo, **PinX**ou células na coluna X de uma seção **Geometry** ) extrair apenas o *x* -coordenar a parte de um valor de ponto. As células que se relacionam com *y* -coordenadas extrair apenas *y* -coordenar a parte de um valor de ponto. 
  
Por exemplo, o Visio extrai a fórmula `PNT(3,4)` dessas três maneiras. 
  
|**Célula**|**Se você digitar**|**O Visio tratará como**|**Resultado**|
|:-----|:-----|:-----|:-----|
| X  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | 3.0000 pol.  <br/> |
| Y  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | 4.0000 pol.  <br/> |
| A-D  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | PNT (3.0000 pol., 4,0000 pol.)  <br/> |
   

