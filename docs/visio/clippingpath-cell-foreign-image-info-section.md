---
title: Célula ClippingPath (Seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contém uma referência à geometria do caminho pelo o que uma imagem está limitada.
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425509"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>Célula ClippingPath (Seção Foreign Image Info)

Contém uma referência à geometria do caminho pelo o que uma imagem está limitada. 
  
## <a name="remarks"></a>Comentários

Se a **célula ClippingPath** aponta para um caminho válido, a imagem é cortada para que a imagem seja renderizada dentro do caminho. Se a **célula ClippingPath** estiver vazia ou contiver uma entrada inválida, a imagem será renderizada com um clipe retangular, usando os valores de escala e deslocamento. 
  
> [!NOTE]
> Somente caminhos definidos [por uma seção Geometry](geometry-section.md) no ShapeSheet da imagem são entradas válidas para a **célula ClippingPath.** Referências entre planilhas não podem ser usadas para definir um caminho de recorte de imagem. 
  
Para fazer referência à célula **ClippingPath** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ClippingPath  <br/> |
   
Para fazer referência à célula **ClippingPath** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowForeign** <br/> |
| Índice de célula:  <br/> |**visFrgnImgClippingPath** <br/> |
   
## <a name="example"></a>Exemplo

Você pode alterar a forma delimitativa de uma imagem para uma oval fazendo o seguinte:
  
- Insira a imagem na tela de desenho.
    
- Clique com o botão direito do mouse na imagem e selecione **Mostrar ShapeSheet**.
    
- Clique com o botão direito do mouse em qualquer lugar no ShapeSheet e selecione **Inserir Seção.**
    
- Na caixa **de diálogo Inserir Seção,** selecione **Geometria e** clique em **OK.**
    
- Na nova seção Geometry (por exemplo, "Geometry2"), exclua apenas uma linha.
    
- Clique com o botão direito do mouse na linha restante e clique em **Alterar Tipo de Linha.**
    
- Na caixa **de diálogo Alterar Tipo** de Linha, selecione **Elipse** e clique em **OK.**
    
- Na seção **Imagem Externa,** de definida a fórmula para a célula **ClippingPath** e aceite  `="Geometry2.Path"` a fórmula. 
    

