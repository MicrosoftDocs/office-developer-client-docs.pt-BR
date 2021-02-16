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
description: 'As fórmulas podem conter sequências de caracteres. Para formatar a saída da sequência, como em uma célula de prompt, um valor de item de dados da forma ou um campo de texto, especifique uma figura de formatação. A saída pode ser formatada como um par de unidade numérica, uma sequência de caracteres, uma data ou hora, uma duração ou uma moeda. Por exemplo, o formato imagem0 #/10 formatará o par de unidades de número de 10,9 cm como 10 9/10 centímetros.'
ms.openlocfilehash: aa95e11db387913edbb40292f7da6a0f4b8a5cf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409514"
---
# <a name="about-strings"></a>Sobre Sequências de Caracteres

As fórmulas podem conter sequências de caracteres. Para formatar a saída da sequência, como em uma célula de prompt, um valor de item de dados da forma ou um campo de texto, especifique uma figura de formatação. A saída pode ser formatada como um par de unidade numérica, uma sequência de caracteres, uma data ou hora, uma duração ou uma moeda. Por exemplo, a figura de formatação "0 #/10 uu" formata o par de unidade numérica 10,9 cm como "10 9/10 centímetros".
  
Você pode usar figuras de formatação **na célula Format** da seção Shape Data e como um argumento para a função **FORMAT** ou **FORMATEX.** Quando você insere um campo de texto, as imagens de formatação são exibidas na lista de formatações da caixa de diálogo **Campo** (guia **Inserir**). 
  
## <a name="using-functions-to-format-strings"></a>Usando funções para formatar sequências de caracteres

Em qualquer fórmula que seja resolvida como uma cadeia de caracteres, incluindo fórmulas de campo de texto personalizadas, você pode usar a **função FORMAT** ou **FORMATEX.** A função FORMAT retorna uma sequência de caracteres da saída formatada. A **função FORMATEX** converte a entrada não formatada para as unidades que você escolher para o resultado formatado. 
  
## <a name="displaying-formatted-shape-data"></a>Exibindo dados de forma formatados

Você pode formatar o valor exibido de um item de dados da forma inserindo uma imagem de formatação na célula Format.
  
Por exemplo, a forma do cronograma de um projeto pode ter um item de dados da forma para medir o custo de um processo. Como padrão, o valor de um item de dados da forma é uma sequência de caracteres. Para formatar a sequência "1200", você pode inserir "$###,###.00" na célula Format de forma que os usuários possam visualizar uma moeda.
  
O Microsoft Visio usa as configurações na guia **Moeda** na caixa de diálogo **Personalizar Formato** no item **Região e Idioma** no Painel de Controle para determinar o símbolo da moeda e o separador de milhar a ser exibido. (No **Painel de Controle,** clique **em Região e Idioma** e clique **em Configurações Adicionais.**
  
Para converter uma sequência de caracteres no valor de uma moeda, de forma que você possa efetuar cálculos com o valor, use a função CY.
  
## <a name="using-functions-to-manipulate-text-strings"></a>Usando funções para manipular sequências de caracteres de texto

É possível usar funções para manipular sequências de caracteres de texto, por exemplo, para localizar ou substituir determinados caracteres em uma sequência de texto. Além disso, você pode obter informações sobre a posição de um caractere em uma sequência ou identificar os caracteres inicial e final em uma sequência de texto. 
  

