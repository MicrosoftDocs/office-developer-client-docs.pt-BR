---
title: Sobre Sequências de Caracteres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251826
localization_priority: Normal
ms.assetid: e1174d8f-70cb-4595-7906-889da15367db
description: 'Fórmulas que podem conter cadeias de caracteres. Para formatar a saída de cadeia de caracteres, como em uma célula prompt, um valor de item de dados da forma ou um campo de texto, você deve especificar uma figura de formatação. Saída pode ser formatada como um par de unidade numérica, cadeia de caracteres, data / hora, duração ou uma moeda. Por exemplo, os uuformats de #/ 10 formato picture0 a unidade de número emparelhar 10,9 cm as10 9/10 centímetros.'
ms.openlocfilehash: 1fd003ecd5c824042e97a40fa8374aeead254ddc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771227"
---
# <a name="about-strings"></a>Sobre cadeias de caracteres

As fórmulas podem conter sequências de caracteres. Para formatar a saída da sequência, como em uma célula de prompt, um valor de item de dados da forma ou um campo de texto, especifique uma figura de formatação. A saída pode ser formatada como um par de unidade numérica, uma sequência de caracteres, uma data ou hora, uma duração ou uma moeda. Por exemplo, a figura de formatação "0 #/10 uu" formata o par de unidade numérica 10,9 cm como "10 9/10 centímetros".
  
Você pode usar figuras de formatação na célula **Format** da seção dados da forma e como um argumento para a função **FORMAT** ou **FORMATEX** . Quando você insere um campo de texto, figuras de formatação aparecem na lista de formatos na caixa de diálogo **campo** (guia**Inserir** ). 
  
## <a name="using-functions-to-format-strings"></a>Usando funções para formatar sequências de caracteres

Em qualquer fórmula que resulta em uma cadeia de caracteres, incluindo fórmulas de campo de texto personalizado, você pode usar a função **FORMAT** ou **FORMATEX** . A função FORMAT retorna uma cadeia de caracteres da saída formatada. A função **FORMATEX** converte a entrada não digitada para as unidades que você escolher para o resultado formatado. 
  
## <a name="displaying-formatted-shape-data"></a>Exibindo dados de forma formatados

Você pode formatar o valor exibido de um item de dados da forma inserindo uma imagem de formatação na célula Format.
  
Por exemplo, a forma do cronograma de um projeto pode ter um item de dados da forma para medir o custo de um processo. Como padrão, o valor de um item de dados da forma é uma sequência de caracteres. Para formatar a sequência "1200", você pode inserir "$###,###.00" na célula Format de forma que os usuários possam visualizar uma moeda.
  
Microsoft Visio utiliza as configurações na guia **moeda** , na caixa de diálogo **Personalizar formato** no item de **região e idioma** no painel de controle para determinar o símbolo de moeda e de milhar separador para exibir. (No **Painel de controle**, clique em **região e idioma**e, em seguida, clique em **Configurações adicionais**).
  
Para converter uma sequência de caracteres no valor de uma moeda, de forma que você possa efetuar cálculos com o valor, use a função CY.
  
## <a name="using-functions-to-manipulate-text-strings"></a>Usando funções para manipular sequências de caracteres de texto

É possível usar funções para manipular sequências de caracteres de texto, por exemplo, para localizar ou substituir determinados caracteres em uma sequência de texto. Além disso, você pode obter informações sobre a posição de um caractere em uma sequência ou identificar os caracteres inicial e final em uma sequência de texto. 
  

