---
title: Função SUM (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Retorna a soma de todos os valores na expressão.
ms.openlocfilehash: b0fed86469b32ddcc7f60a388f5d42c7bbd48b6c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304232"
---
# <a name="sum-function-access-custom-web-app"></a>Função SUM (aplicativo Web personalizado do Access)

Retorna a soma de todos os valores na expressão.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 **Soma** (*Numericé*) 
  
A função **sum** contém o argumento a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Numericé*  <br/> |Uma expressão que identifica o campo que contém os dados numéricos que você deseja adicionar ou uma expressão que executa um cálculo usando os dados desse campo. Os operandos na *numeric* Express podem incluir o nome de um campo de tabela, uma constante ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções agregaDAS do SQL).  <br/> |
   
## <a name="remarks"></a>Comentários

A função **sum** ignora registros que contenham valores nulos. 
  
A função **sum** só pode ser usada com colunas numéricas. 
  

