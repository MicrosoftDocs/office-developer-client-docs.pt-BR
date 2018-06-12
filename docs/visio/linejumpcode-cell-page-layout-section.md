---
title: Célula LineJumpCode (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Determina os conectores aos quais você deseja adicionar saltos.
ms.openlocfilehash: abb7208c2cfbd6b1423e091efc1d526f8b10b57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772190"
---
# <a name="linejumpcode-cell-page-layout-section"></a>Célula LineJumpCode (Seção Page Layout)

Determina os conectores aos quais você deseja adicionar saltos.
  
|**Valor**|**Conectores aos quais você deseja adicionar saltos**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Nenhum  <br/> |**visPLOJumpNone** <br/> |
|1  <br/> |Linhas horizontais  <br/> |**visPLOJumpHorizontal** <br/> |
|2  <br/> |Linhas verticais  <br/> |**visPLOJumpVertical** <br/> |
|3  <br/> |Última linha circulada  <br/> |**visPLOJumpLastRouted** <br/> |
|4  <br/> |Última linha exibida (primeira forma na *z* -ordem)  <br/> |**visPLOJumpDisplayOrder** <br/> |
|5  <br/> |Primeira linha exibida (forma no fim de a *z* -ordem)  <br/> |**visPLOJumpReverseDisplayOrder** <br/> |
   
## <a name="remarks"></a>Coment�rios

Você também pode definir o valor dessa célula na guia **Layout e roteamento** na caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** e, em seguida, clique em **Layout e roteamento**).
  
Para obter uma referência para a célula LineJumpCode pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LineJumpCode  <br/> |
   
Para obter uma referência para a célula LineJumpCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPageLayout** <br/> |
|Índice da célula:  <br/> |**visPLOJumpCode** <br/> |
   

