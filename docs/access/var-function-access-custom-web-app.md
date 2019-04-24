---
title: Função var (aplicativo da Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Retorna a variância estatística de uma amostra de população representada como um conjunto de valores contidos em um campo especificado em uma consulta.
ms.openlocfilehash: 80cea512b0386d9b0461c927675ae51be3e0dcda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304197"
---
# <a name="var-function-access-custom-web-app"></a>Função var (aplicativo da Web personalizado do Access)

Retorna a variância estatística de uma amostra de população representada como um conjunto de valores contidos em um campo especificado em uma consulta.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 **Var** (*Numericé*) 
  
A função **var** contém o argumento a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Numericé*  <br/> |Uma expressão de texto que identifica o campo que contém os dados numéricos que você deseja avaliar ou uma expressão que executa um cálculo usando os dados desse campo. Os operandos na *numeric* Express podem incluir o nome de um campo de tabela, uma constante ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções agregaDAS do SQL).  <br/> |
   
## <a name="remarks"></a>Comentários

 **Var** só pode ser usado com colunas numéricas. Valores nulos são ignorados. 
  

