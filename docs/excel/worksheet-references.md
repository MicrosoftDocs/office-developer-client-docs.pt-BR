---
title: Referências de planilha
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- referências [excel 2007], planilha, referências de planilha [Excel 2007],referências de planilha externa [Excel 2007],planilha ativa [Excel 2007],planilha atual [Excel 2007],referências de planilha internas [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2944f73a3144837a4be8aff7c7fed9a8d2158203
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416458"
---
# <a name="worksheet-references"></a>Referências de planilha

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Uma referência no Microsoft Excel é um tipo de dados que se refere a um bloco retangular de células (que pode ser apenas uma célula) ou, em alguns casos, a um número de blocos de células não adjacentes. Internamente, o Excel usa um tipo de referência para células na planilha atual, conhecida como referência interna. Qualquer célula que não está na planilha atual é descrita por outro tipo de referência conhecido como referência externa. Consulte a próxima seção para a definição de ativo e atual.
  
## <a name="active-vs-current"></a>Active vs. Current

No Excel, o termo ativo refere-se ao que o usuário está exibindo. A pasta de trabalho e a planilha ativas são aquelas que o usuário está olhando no momento ou, se o Excel tiver perdido o foco para outro aplicativo, estava olhando quando o Excel teve o foco pela última vez. A planilha ativa está sempre na pasta de trabalho ativa. As células selecionadas na planilha ativa são conhecidas como células ativas. Se um objeto incorporado tiver foco, as células selecionadas por último ainda estão ativas. 
  
O termo atual se refere ao que o Excel está recalculando. A pasta de trabalho e a planilha atuais são aquelas que estão sendo recalculadas no momento. A planilha atual está sempre na pasta de trabalho atual. A célula recalculada é conhecida como a célula atual ou, no caso de uma fórmula de matriz sendo recalculada, as células atuais. 
  
Os pontos importantes a lembrar são:
  
- A pasta de trabalho/planilha/célula ativa geralmente não é a atual, embora possa ser.
    
- Uma função de add-in, seja em um módulo do Visual Basic for Applications (VBA) ou em uma DLL ou XLL, é sempre chamada a partir da célula atual na planilha atual, ou uma delas no caso de MTR (recálculo multithread).
    
Muitas funções do Excel que fornecem informações sobre uma célula, um intervalo de células ou uma planilha em uma pasta de trabalho distinguem entre a pasta de trabalho ativa, planilha ou célula e a pasta de trabalho atual, planilha ou célula. Essa diferença é refletida nos tipos de dados usados para descrever referências a blocos de células, conforme descrito na seção a seguir.
  
## <a name="internal-and-external-worksheet-references"></a>Referências de Planilha Interna e Externa

A principal diferença entre referências internas e externas é que o tipo de dados de referência externa contém uma ID para a planilha e também uma descrição à qual as células são referenciadas. Uma referência interna não contém referência à planilha— é implícito que a planilha é a planilha atual. 
  
Muitas funções da API de C retornam referências ou levam argumentos de referência. Qualquer função da API de C que aceita argumentos de referência aceita referências internas ou externas, exceto a **função xlSheetNm,** que requer uma referência externa. Algumas funções retornam apenas referências internas ou externas. Por exemplo, a função [xlfCaller](xlfcaller.md) da API C retorna uma referência às células de chamada, por definição, na planilha atual. A referência retornada é sempre uma referência interna, embora a função possa retornar tipos de não referência onde a função não é chamada de uma célula de planilha. A função da API de C [xlSheetId](xlsheetid.md) sempre retorna a ID de uma planilha contida em um tipo de dados de referência externa. 
  
A outra diferença importante entre os tipos de referência interna e externa é que o tipo de dados de referência externa pode descrever vários blocos não adjacentes de células na mesma planilha. As referências internas podem descrever apenas um único bloco na planilha atual. Referências não adjacentes podem ser passadas para qualquer função que aceita um argumento de intervalo.
  
## <a name="see-also"></a>Confira também



[Conceitos de programação do Excel](excel-programming-concepts.md)
  
[Avaliar nomes e outras expressões de fórmula de planilha](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Avaliação de expressões e planilhas do Excel](excel-worksheet-and-expression-evaluation.md)

