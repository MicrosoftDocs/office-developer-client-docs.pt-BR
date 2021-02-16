---
title: Função Var (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Retorna a variação estatística de uma amostra da população representada como um conjunto de valores contidos em um campo especificado em uma consulta.
ms.openlocfilehash: 80cea512b0386d9b0461c927675ae51be3e0dcda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437753"
---
# <a name="var-function-access-custom-web-app"></a>Função Var (aplicativo Web personalizado do Access)

Retorna a variação estatística de uma amostra da população representada como um conjunto de valores contidos em um campo especificado em uma consulta.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 **Var** (*NumericExpression*) 
  
A **função Var** contém o argumento a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *NumericExpression*  <br/> |Uma expressão de texto que identifica o campo que contém os dados numéricos que você deseja avaliar ou uma expressão que executa um cálculo usando os dados desse campo. Os operands em  *NumericExpression*  podem incluir o nome de um campo de tabela, uma constante ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções sql agregadas).  <br/> |
   
## <a name="remarks"></a>Comentários

 **Var** pode ser usado somente com colunas numéricas. Valores nulos são ignorados. 
  

