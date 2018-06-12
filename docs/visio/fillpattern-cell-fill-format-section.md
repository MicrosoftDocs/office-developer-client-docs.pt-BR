---
title: Célula FillPattern (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Determina o padrão de preenchimento da forma. Para especificar um padrão de preenchimento personalizado, utilize a função USE da célula.
ms.openlocfilehash: 26429e06ad432eaf7fae9188ac676cb4be3201c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771880"
---
# <a name="fillpattern-cell-fill-format-section"></a>Célula FillPattern (Seção Fill Format)

Determina o padrão de preenchimento da forma. Para especificar um padrão de preenchimento personalizado, utilize a função USE da célula.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Nenhum (preenchimento transparente).  <br/> |
|1  <br/> |Cor do primeiro plano sólida.  <br/> |
|2 - 40  <br/> |Padrões de preenchimento variados correspondentes a entradas indexadas na caixa de diálogo **preenchimento** .  <br/> |
   
## <a name="remarks"></a>Coment�rios

Você também pode definir o valor utilizando a caixa de diálogo **preenchimento** (na guia **página inicial** , no grupo **forma** , clique em **preenchimento** e, em seguida, clique em **Opções de preenchimento**).
  
Para obter uma referência para a célula FillPattern pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |FillPattern  <br/> |
   
Para obter uma referência para a célula FillPattern pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowFill** <br/> |
|Índice da célula:  <br/> |**visFillPattern** <br/> |
   

