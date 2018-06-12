---
title: Função VAR (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Retorna a variância estatística para uma amostra da população representada como um conjunto de valores contidos em um campo especificado em uma consulta.
ms.openlocfilehash: 9937f1985c0a7df5eb06977333ab889947891380
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765254"
---
# <a name="var-function-access-custom-web-app"></a>Função VAR (aplicativo da web personalizado do Access)

Retorna a variância estatística para uma amostra da população representada como um conjunto de valores contidos em um campo especificado em uma consulta.
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Syntax

 **Var** (*NumericExpression*) 
  
A função **Var** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *NumericExpression*  <br/> |Uma expressão de texto que identifica o campo que contém os dados numéricos que você deseja avaliar ou uma expressão que executa um cálculo usando os dados nesse campo. Operandos em *NumericExpression* podem incluir o nome de um campo de tabela, uma constante ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções SQL agregadas).  <br/> |
   
## <a name="remarks"></a>Coment�rios

 **Var** pode ser usado com somente colunas numéricas. Valores nulos são ignorados. 
  

