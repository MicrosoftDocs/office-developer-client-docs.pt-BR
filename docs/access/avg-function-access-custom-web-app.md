---
title: Função AVG (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Calcula a média aritmética de um conjunto de valores contidos em um campo especificado.
ms.openlocfilehash: afe832a51fc9cd3b224087a0b06fe539f6a7004b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765061"
---
# <a name="avg-function-access-custom-web-app"></a>Função AVG (aplicativo da web personalizado do Access)

Calcula a média aritmética de um conjunto de valores contidos em um campo especificado.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 **Avg** (*NumericExpression*) 
  
A função **Avg** contém os seguintes argumentos. 
  
|**Argumento**|**Descrição**|
|:-----|:-----|
|NumericExpression  <br/> |Uma expressão de cadeia de caracteres que identifica o campo que contém os dados numéricos que você deseja média ou uma expressão que executa um cálculo usando os dados nesse campo. Operandos em *NumericExpression* podem incluir o nome de um campo de tabela, uma variável ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções SQL agregadas).  <br/> |
   
## <a name="remarks"></a>Comentários

A média calculada por **Avg** é a média aritmética (a soma dos valores divididos pelo número de valores). Por exemplo, use **Avg**, para calcular o custo médio do frete. 
  
A função **Avg** não inclui qualquer valores **Nulos** no cálculo. 
  

