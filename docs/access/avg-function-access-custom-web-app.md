---
title: Função AVG (aplicativo da Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Calcula a média aritmética de um conjunto de valores contidos em um campo especificado.
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426720"
---
# <a name="avg-function-access-custom-web-app"></a>Função AVG (aplicativo da Web personalizado do Access)

Calcula a média aritmética de um conjunto de valores contidos em um campo especificado.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 **Méd** (*Numericé*) 
  
A função **AVG** contém o argumento a seguir. 
  
|**Argumento**|**Descrição**|
|:-----|:-----|
|Numericé  <br/> |Uma expressão de cadeia de caracteres identificando o campo que contém os dados numéricos que você deseja média ou uma expressão que executa um cálculo usando os dados desse campo. Os operandos na *numeric* Express podem incluir o nome de um campo de tabela, uma variável ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções agregaDAS do SQL).  <br/> |
   
## <a name="remarks"></a>Comentários

A média calculada por **Avg** é a média aritmética (a soma dos valores divididos pelo número de valores). Por exemplo, use **Avg**, para calcular o custo médio do frete. 
  
A função **AVG** não inclui nenhum valor **nulo** no cálculo. 
  

