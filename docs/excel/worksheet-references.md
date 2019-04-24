---
title: Referências de planilha
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- referências [Excel 2007], planilha, referências de planilha [Excel 2007], referência externa de planilha [Excel 2007], planilha ativa [Excel 2007], planilha atual [Excel 2007], referências de planilha internas [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2944f73a3144837a4be8aff7c7fed9a8d2158203
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304022"
---
# <a name="worksheet-references"></a>Referências de planilha

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Uma referência no Microsoft Excel é um tipo de dados que se refere a um bloco retangular de células (que pode ser apenas uma célula) ou, em alguns casos, vários blocos de não-junção de células. Internamente, o Excel usa um tipo de referência para células na planilha atual, conhecido como referência interna. Qualquer célula que não esteja na planilha atual é descrita por outro tipo de referência conhecido como uma referência externa. ConFira a próxima seção para a definição de ativo e atual.
  
## <a name="active-vs-current"></a>Ativo versus atual

No Excel, o termo ativo se refere ao que o usuário está exibindo. As pastas de trabalho e planilhas ativas são aquelas que o usuário está vendo atualmente ou, se o Excel tiver perdido o foco para outro aplicativo, estava examinando quando o Excel teve o foco pela última vez. A planilha ativa está sempre na pasta de trabalho ativa. Uma ou mais células selecionadas na planilha ativa são conhecidas como células ativas. Se um objeto incorporado tiver o foco, as células selecionadas por último ainda estarão ativas. 
  
O termo atual se refere ao que o Excel está recalculando. A pasta de trabalho atual e a planilha são aquelas que estão sendo recalculadas no momento. A planilha atual está sempre na pasta de trabalho atual. A célula que está sendo recalculada é conhecida como a célula atual ou, no caso de uma fórmula de matriz sendo recalculada, as células atuais. 
  
Os pontos importantes a serem lembrados são os seguintes:
  
- A pasta de trabalho/planilha/célula ativa não é geralmente a atual, embora possa ser.
    
- Uma função de suplemento, em um módulo do Visual Basic for Applications (VBA) ou uma DLL ou XLL, é sempre chamada da célula atual na planilha atual ou uma delas no caso de recálculo de vários threads (MTR).
    
Muitas funções do Excel que fornecem informações sobre uma célula, um intervalo de células ou uma planilha em uma pasta de trabalho distingue entre a pasta de trabalho ativa, a planilha ou a célula e a pasta de trabalho, planilha ou célula atual. Essa diferença é refletida nos tipos de dados usados para descrever referências a blocos de células, conforme descrito na seção a seguir.
  
## <a name="internal-and-external-worksheet-references"></a>Referências de planilha interna e externa

A principal diferença entre referências internas e externas é que o tipo de dados de referência externa contém uma ID da planilha e também uma descrição de quais células são referenciadas. Uma referência interna não contém nenhuma referência à planilha — é implícito que a planilha é a planilha atual. 
  
Muitas funções da API de C retornam referências ou levam argumentos de referência. Qualquer função da API de C que aceita argumentos de referência aceita referências internas ou externas, exceto a função **xlSheetNm** , que requer uma referência externa. Algumas funções retornam apenas referências internas ou externas. Por exemplo, a função da API C [xlfCaller](xlfcaller.md) retorna uma referência às células de chamada, por definição, na planilha atual. A referência retornada é sempre uma referência interna, embora a função possa retornar tipos que não são de referência, onde a função não é chamada a partir de uma célula de planilha. A função da API C [xlSheetId](xlsheetid.md) sempre retorna a ID de uma planilha contida em um tipo de dados de referência externa. 
  
A outra diferença importante entre os tipos de referência interna e externa é que o tipo de dados de referência externa pode descrever vários blocos de disjunção de células na mesma planilha. As referências internas podem descrever apenas um único bloco na planilha atual. As referências de disjunção podem ser passadas para qualquer função que usa um argumento Range.
  
## <a name="see-also"></a>Confira também



[Conceitos de programação do Excel](excel-programming-concepts.md)
  
[Avaliar nomes e outras expressões de fórmula de planilha](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Avaliação de expressões e planilhas do Excel](excel-worksheet-and-expression-evaluation.md)

