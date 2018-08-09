---
title: Célula ClippingPath (Seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contém uma referência para a geometria do caminho que uma imagem limitada por.
ms.openlocfilehash: 9f1c159e303c1d7bc3467c36756a422a3f325c7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771500"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>Célula ClippingPath (Seção Foreign Image Info)

Contém uma referência para a geometria do caminho que uma imagem limitada por. 
  
## <a name="remarks"></a>Comentários

Se a célula **ClippingPath** aponta para um caminho válido, a imagem é cortada para que a imagem é processada dentro do caminho. Se a célula **ClippingPath** está vazia ou contém uma entrada inválida, em seguida, a imagem será processada com um clipe retangular, usando os valores de deslocamento e escala. 
  
> [!NOTE]
> Somente os caminhos definidos por uma seção [Geometry](geometry-section.md) na ShapeSheet da imagem são entradas válidas para a célula **ClippingPath** . Referências entre planilhas não podem ser usadas para definir um caminho de recorte de imagem. 
  
Para fazer referência à célula **ClippingPath** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ClippingPath  <br/> |
   
Para obter uma referência à célula **ClippingPath** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowForeign** <br/> |
| Índice da célula:  <br/> |**visFrgnImgClippingPath** <br/> |
   
## <a name="example"></a>Exemplo

Você pode alterar a forma de contorno de uma imagem para uma elipse fazendo o seguinte:
  
- Insira a imagem para a tela de desenho.
    
- A imagem do mouse em e selecione **Mostrar ShapeSheet**.
    
- Com o botão direito em qualquer lugar na ShapeSheet e selecione **Inserir seção**.
    
- Na caixa de diálogo **Inserir seção** , selecione a **geometria** e clique em **Okey**.
    
- Na seção Geometry novo (por exemplo, "Geometry2"), exclua apenas uma fila.
    
- Com o botão direito na linha restante e clique em **Alterar tipo de linha**.
    
- Na caixa de diálogo **Alterar tipo de linha** , selecione **Elipse** e clique em **Okey**.
    
- Na seção **Foreign Image** , defina a fórmula para a célula **ClippingPath** para `="Geometry2.Path"` e aceite a fórmula. 
    

