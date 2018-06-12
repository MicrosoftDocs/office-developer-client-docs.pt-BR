---
title: Referências de planilha
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- referências [excel 2007], planilha, referências de planilha [Excel 2007], referências de planilha externos [Excel 2007], a planilha ativa [Excel 2007], planilha atual [Excel 2007], planilha interna referencia [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7089fb891c96be9182189e3a5f30057721cebbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765458"
---
# <a name="worksheet-references"></a>Referências de planilha

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Uma referência no Microsoft Excel é um tipo de dados que se refere a um bloco retangular de células (que podem ser uma única célula) ou em alguns casos, um número de blocos não contíguas de células. Internamente, o Excel usa um tipo de referência para as células na planilha atual, conhecido como uma referência interna. Qualquer célula que não esteja na planilha atual é descrita por outro tipo de referência, conhecido como uma referência externa. Consulte a próxima seção para a definição de ativo e atual.
  
## <a name="active-vs-current"></a>Active versus atual

No Excel, o termo ativo refere-se para o usuário está exibindo. A pasta de trabalho ativa e uma planilha são aquelas que o usuário está atualmente olhando ou, se o Excel perde o foco para outro aplicativo, buscava em quando Excel última tinha o foco. A planilha ativa é sempre na pasta de trabalho ativa. Uma ou mais células selecionadas na planilha ativa são conhecidas como das células ativas. Se um objeto incorporado tiver o foco, as células selecionadas pelo último ainda estão ativas. 
  
O termo atual se refere ao Excel o que é recalcular. A pasta de trabalho atual e a planilha são aquelas que atualmente estão sendo recalculada. A planilha atual é sempre na pasta de trabalho atual. A célula seja recalculada é conhecida como a célula atual, ou, no caso de uma fórmula de matriz seja recalculado, as células atuais. 
  
Os pontos importantes lembrar são:
  
- A pasta de trabalho/planilha/célula ativa não é geralmente aquela atual, embora ele pode ser.
    
- Uma função add-in, se está em um Visual Basic for Applications (VBA) módulo, ou como uma DLL ou XLL, é sempre chamada da célula atual na planilha atual, ou uma no caso de recálculo multithreaded (MTR).
    
Várias funções do Excel que fornecem informações sobre uma célula, um intervalo de células ou uma planilha em uma pasta de trabalho distinguir entre a pasta de trabalho ativa, planilha, ou célula e a pasta de trabalho atual, planilha ou célula. Essa diferença é refletida nos tipos de dados usados para descrever as referências a blocos de células, conforme descrito na seção a seguir.
  
## <a name="internal-and-external-worksheet-references"></a>Referências de planilha internas e externas

A principal diferença entre referências internas e externas é que o tipo de dados de referência externa contém uma ID para a planilha e também uma descrição dos quais células são chamadas. Uma referência interna não contém nenhuma referência à planilha — é implícito que a planilha é a planilha atual. 
  
Muitas funções da API C retornam referências ou levam argumentos de referência. Qualquer função de API C que leva referência argumentos aceita referências internas ou externas, exceto a função **xlSheetNm** , que requer uma referência externa. Algumas funções retornam apenas referências internas ou externas. Por exemplo, a função do C API [xlfCaller](xlfcaller.md) retorna uma referência para as células de chamada, por definição, na planilha atual. A referência retornada é sempre uma referência interna, embora a função pode retornar tipos de não-referência onde a função não é chamada de uma célula da planilha. A função do C API [xlSheetId](xlsheetid.md) sempre retorna a ID de uma planilha contida em um tipo de dados de referência externa. 
  
As diferenças importantes entre os tipos de referência interna e externa é que o tipo de dados de referência externa pode descrever vários blocos não contíguas de células na mesma folha. Referências internas podem descrever somente um único bloco na planilha atual. Referências não contíguas podem ser passadas para qualquer função que usa um argumento de intervalo.
  
## <a name="see-also"></a>Confira também



[Excel Programming Concepts](excel-programming-concepts.md)
  
[Avaliando os nomes e outras expressões de fórmula de planilha](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Planilha do Excel e avaliação de expressão](excel-worksheet-and-expression-evaluation.md)

