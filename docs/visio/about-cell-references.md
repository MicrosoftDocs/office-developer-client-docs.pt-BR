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
ms.openlocfilehash: 54c7fd69e2ddaa9350996e2d8c921958a04e34ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771233"
---
# <a name="about-cell-references"></a>Sobre Referências de Célula

É possível criar interdependências entre as fórmulas por meio das referências de célula ShapeSheet. As referências de célula permitem calcular um valor para uma célula com base no valor de outra célula. Por exemplo, a célula Width pode conter uma fórmula que calcule a largura da forma consultando valor de sua célula Height, de modo que, quando um usuário redimensionar a forma verticalmente, sua largura será definida proporcionalmente.
  
Na fórmula de uma célula, você pode fazer referência a uma célula da mesma forma ou de um outro objeto, como um documento ou uma página, para que o Microsoft Visio calcule o valor de uma célula com base no valor de uma outra.
  
## <a name="what-cell-references-can-include"></a>Referências de célula podem incluir

Referências de célula podem incluir identificações de forma (IDs) ou nomes. Você sempre pode consultar a qualquer forma na página pela sua ID, se a forma é nomeada ou não. Se uma forma não tiver sido nomeada, seu nome padrão é folha. *i* , onde *i* é o ID da forma. A ID é atribuída quando a forma é criada e não muda, a menos que você mova a forma para outra página ou documento. Se mais de uma forma em uma página tem o mesmo nome, você deve incluir a ID atribuída. 
  
## <a name="cell-reference-syntax-and-examples"></a>Sintaxe de referência de célula e exemplos

A sintaxe usada e a possibilidade de fazer referência a uma forma pelo nome dependem da relação entre os dois objetos. Estas regras gerais podem ser aplicadas:
  
- Se uma forma for um ponto a ponto de uma forma cuja fórmula esteja sendo editada, será possível fazer referência à forma ponto a ponto pelo nome. Se essa forma for um grupo, você poderá fazer referência ao grupo pelo nome, mas não por seus membros. Não é possível fazer referência a um pai da forma nem a suas formas ponto a ponto pelo nome.
    
- É possível usar a sintaxe Sheet.ID para fazer referência a qualquer forma na página, independentemente se a forma estiver em um grupo ou for pai de uma forma.
    
- Nomes que contenham caracteres que não sejam padrão devem ser inseridos entre aspas simples. Os caracteres entre aspas simples em um nome que não seja padrão devem ser precedidos por uma aspa simples.
    
|**Para fazer referência a uma célula de**|**Use esta sintaxe**|**Exemplo**|
|:-----|:-----|:-----|
|Mesma forma  <br/> | Nome da célula  <br/> | Largura  <br/> |
| Uma forma, um grupo ou uma guia  <br/> | Shapename! Nome da célula  <br/> | Estrela! Ângulo  <br/> |
| Uma forma, um grupo ou uma guia em que mais de uma forma no mesmo nível tenha o mesmo nome  <br/> | Shapename.ID! Nome da célula  <br/> | Executive.2! Altura  <br/> |
| Uma coluna nomeada com linhas indexadas  <br/> | Section.Column[index]  <br/> | Char.Font[3]  <br/> |
| Uma coluna não-nomeada com linhas indexadas  <br/> | Section.ColumnIndex  <br/> | Scratch.A5  <br/> |
| Qualquer forma, página, mestre ou estilo  <br/> | Sheet.ID! Nome da célula  <br/> | Sheet.8! FillForegnd  <br/> |
| Um mestre  <br/> | Masters [MasterName]! Nome da planilha! Referênciadecélula  <br/> | Mestres [engrenagem]! Eixo! Geometry1.x1  <br/> |
| A página ou a página mestra na qual o objeto está localizado  <br/> | Página! Referênciadecélula  <br/> | Página! User.Vanishing_Point  <br/> |
| Outra página no documento  <br/> | Páginas [PageName]! Nome da planilha! Referênciadecélula  <br/> | Páginas [página-3]! Sheet.4! BeginX  <br/> |
| Um estilo  <br/> | Estilos! Nome da planilha! Referênciadecélula  <br/> | Estilos! Gerente! LineColor  <br/> |
| O documento  <br/> | TheDoc! Referênciadecélula  <br/> | TheDoc! PreviewQuality  <br/> |
| Uma forma, página, mestre, documento ou estilo com um nome não padrão.  <br/> | 'Sheetname'! Nome da célula  <br/> | ' 1-D'! LineColor  <br/> |
   

