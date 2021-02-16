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
ms.openlocfilehash: a7d2c6762e96fc19986521c2ba164666b925c928
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411600"
---
# <a name="scratch-section"></a>Seção Scratch

Uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.
  
## <a name="remarks"></a>Comentários

É possível adicionar essa seção usando a caixa de diálogo **Inserir Seção**. Clique com o botão direito do mouse na janela do ShapeSheet e clique em **Inserir Seção**.
  
A **seção Scratch** é normalmente usada para isolar cálculos complexos repetidos. Se a sua solução tiver um objetivo bem definido, é mais sensato usar uma célula na seção **User-Defined Cells** para maior clareza, pois as células do usuário podem ser nomeadas. 
  
As células na **seção Scratch** usam unidades de duas maneiras diferentes. As células X e Y usam unidades de desenho; as células de A a D não usam unidades. (No jargão dos programadores de C, as células X e Y são "digitadas" e as células de A a D são "nulas". As células **Scratch X** e **Scratch Y** são frequentemente usadas para derivar coordenadas *x* e *y,* como **PinX** e **PinY,** ou as células X e Y encontradas em uma célula da seção **Geometry.** As células de A a D da seção Scratch podem exibir qualquer unidade que for especificada. 
  
Outra diferença é a maneira com que essas células armazenam valores de ponto. Um ponto no Visio é um único pacote de dados para uma coordenada ( *x,y).* Quando uma fórmula retorna um valor de ponto, esse valor pode ser interpretado de três formas, que dependerá em que célula ShapeSheet a fórmula se encontra. As células relacionadas a coordenadas  *x*  (por exemplo, **PinX** ou células na coluna X de uma seção **Geometry)** extraem apenas a parte da coordenada  *x*  de um valor de ponto. As células relacionadas  *a coordenadas y*  extraem apenas a parte da coordenada  *y*  de um valor de ponto. 
  
Por exemplo, o Visio extrai a fórmula  `PNT(3,4)` dessas três maneiras. 
  
|**Cell**|**Se você digitar**|**O Visio tratará como**|**Resultado**|
|:-----|:-----|:-----|:-----|
| X  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | 3.0000 pol.  <br/> |
| S  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | 4.0000 pol.  <br/> |
| A-D  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | PNT(3,0000 in., 4,0000 in.)  <br/> |
   

