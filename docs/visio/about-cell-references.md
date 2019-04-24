---
title: Sobre Referências de Célula
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251827
localization_priority: Normal
ms.assetid: e6a9aceb-90d7-fb53-eaf4-416a1ae2a98b
description: É possível criar interdependências entre as fórmulas por meio das referências de célula ShapeSheet. As referências de célula permitem calcular um valor para uma célula com base no valor de outra célula. Por exemplo, a célula Width pode conter uma fórmula que calcule a largura da forma consultando valor de sua célula Height, de modo que, quando um usuário redimensionar a forma verticalmente, sua largura será definida proporcionalmente.
ms.openlocfilehash: a92bcc560c535dc012ec5cb79db72250e78364c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332617"
---
# <a name="about-cell-references"></a>Sobre Referências de Célula

É possível criar interdependências entre as fórmulas por meio das referências de célula ShapeSheet. As referências de célula permitem calcular um valor para uma célula com base no valor de outra célula. Por exemplo, a célula Width pode conter uma fórmula que calcule a largura da forma consultando valor de sua célula Height, de modo que, quando um usuário redimensionar a forma verticalmente, sua largura será definida proporcionalmente.
  
Na fórmula de uma célula, você pode fazer referência a uma célula da mesma forma ou de um outro objeto, como um documento ou uma página, para que o Microsoft Visio calcule o valor de uma célula com base no valor de uma outra.
  
## <a name="what-cell-references-can-include"></a>O que as referências de célula podem incluir

As referências de célula podem incluir identificações de forma (IDs) ou nomes. Você sempre pode fazer referência a qualquer forma na página pela sua ID, independentemente de a forma estar nomeada ou não. Se a forma não tiver sido nomeada, seu nome padrão será Sheet. *i* , onde *i* é a ID da forma. A ID é atribuída quando a forma é criada e não é alterada a menos que você mova a forma para outra página ou documento. Se mais de uma forma na página tiver o mesmo nome, inclua a ID atribuída. 
  
## <a name="cell-reference-syntax-and-examples"></a>Sintaxe e exemplo de referência de células

A sintaxe usada e a possibilidade de fazer referência a uma forma pelo nome dependem da relação entre os dois objetos. Estas regras gerais podem ser aplicadas:
  
- Se uma forma for um ponto a ponto de uma forma cuja fórmula esteja sendo editada, será possível fazer referência à forma ponto a ponto pelo nome. Se essa forma for um grupo, você poderá fazer referência ao grupo pelo nome, mas não por seus membros. Não é possível fazer referência a um pai da forma nem a suas formas ponto a ponto pelo nome.
    
- É possível usar a sintaxe Sheet.ID para fazer referência a qualquer forma na página, independentemente se a forma estiver em um grupo ou for pai de uma forma.
    
- Nomes que contenham caracteres que não sejam padrão devem ser inseridos entre aspas simples. Os caracteres entre aspas simples em um nome que não seja padrão devem ser precedidos por uma aspa simples.
    
|**Para fazer referência a uma célula de**|**Use esta sintaxe**|**Exemplo**|
|:-----|:-----|:-----|
|Mesma forma  <br/> | Cellname  <br/> | Largura  <br/> |
| Uma forma, um grupo ou uma guia  <br/> | Shapename! Cellname  <br/> | Começando! Reto  <br/> |
| Uma forma, um grupo ou uma guia em que mais de uma forma no mesmo nível tenha o mesmo nome  <br/> | Shapename.ID! Cellname  <br/> | Executivo. 2! Height  <br/> |
| Uma coluna nomeada com linhas indexadas  <br/> | Seção. Column [index]  <br/> | Char. Font [3]  <br/> |
| Uma coluna não-nomeada com linhas indexadas  <br/> | Section. ColumnIndex  <br/> | Scratch. a5  <br/> |
| Qualquer forma, página, mestre ou estilo  <br/> | Sheet.ID! Cellname  <br/> | Sheet. 8! FillForegnd  <br/> |
| Um mestre  <br/> | Mestres [MasterName]! SheetName! CellReference  <br/> | Mestres [engrenagem]! Eixo! Geometry1. X1  <br/> |
| Página ou página mestre na qual o objeto está localizado  <br/> | A página! CellReference  <br/> | A página! User. Vanishing_Point  <br/> |
| Outra página no documento  <br/> | Páginas [pagename]! SheetName! CellReference  <br/> | Páginas [Page-3]! Sheet. 4! BeginX  <br/> |
| Um estilo  <br/> | Estilos! SheetName! CellReference  <br/> | Estilos! Gerenciador! LineColor  <br/> |
| Documento  <br/> | TheDoc! CellReference  <br/> | TheDoc! PreviewQuality  <br/> |
| Uma forma, uma página, um mestre, um documento ou um estilo com um nome que não seja padrão.  <br/> | ' SheetName '! Cellname  <br/> | ' 1-D '! LineColor  <br/> |
   

