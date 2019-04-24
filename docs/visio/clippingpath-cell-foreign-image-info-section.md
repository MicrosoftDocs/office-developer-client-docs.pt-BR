---
title: Célula ClippingPath (seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contém uma referência à geometria do caminho para o qual uma imagem está limitada.
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341857"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>Célula ClippingPath (seção Foreign Image Info)

Contém uma referência à geometria do caminho para o qual uma imagem está limitada. 
  
## <a name="remarks"></a>Comentários

Se a célula **ClippingPath** apontar para um caminho válido, a imagem será recortada para que a imagem seja renderizada dentro do caminho. Se a célula **ClippingPath** estiver vazia ou contiver uma entrada inválida, a imagem será renderizada com um clipe retangular, usando os valores de Scale e offset. 
  
> [!NOTE]
> Somente caminhos definidos por uma seção [Geometry](geometry-section.md) no ShapeSheet da imagem são entradas válidas para a célula **ClippingPath** . Referências de folha cruzada não podem ser usadas para definir um caminho de recorte de imagem. 
  
Para obter uma referência para a célula **ClippingPath** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ClippingPath  <br/> |
   
Para obter uma referência para a célula **ClippingPath** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowForeign** <br/> |
| Índice da célula:  <br/> |**visFrgnImgClippingPath** <br/> |
   
## <a name="example"></a>Exemplo

Você pode alterar a forma de limite de uma imagem para uma elipse fazendo o seguinte:
  
- Insira a imagem na tela de desenho.
    
- Clique com o botão direito do mouse na imagem e selecione **Mostrar ShapeSheet**.
    
- Clique com o botão direito do mouse em qualquer lugar na ShapeSheet e selecione **Inserir seção**.
    
- Na caixa de diálogo **Inserir seção** , selecione **geometria** e clique em **OK**.
    
- Na nova seção Geometry (por exemplo, "Geometry2"), exclua todas exceto uma linha.
    
- Clique com o botão direito do mouse na linha restante e clique em **alterar tipo de linha**.
    
- Na caixa de diálogo **alterar tipo de linha** , selecione **elipse** e clique em **OK**.
    
- Na seção **imagem estrangeira** , defina a fórmula da célula **ClippingPath** como `="Geometry2.Path"` e aceite a fórmula. 
    

