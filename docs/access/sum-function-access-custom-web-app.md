---
title: Função SUM (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Retorna a soma de todos os valores na expressão.
ms.openlocfilehash: 98531a0487505c24ed62034b7c283b9765a3e7a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765242"
---
# <a name="sum-function-access-custom-web-app"></a>Função SUM (aplicativo da web personalizado do Access)

Retorna a soma de todos os valores na expressão.
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Syntax

 **Soma** (*NumericExpression*) 
  
A função **soma** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *NumericExpression*  <br/> |Uma expressão que identifica o campo que contém os dados numéricos que você deseja adicionar ou uma expressão que executa um cálculo usando os dados nesse campo. Operandos em *NumericExpression* podem incluir o nome de um campo de tabela, uma constante ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções SQL agregadas).  <br/> |
   
## <a name="remarks"></a>Coment�rios

A função **soma** ignora registros que contenham valores nulos. 
  
A função **soma** só pode ser usada com colunas numéricas. 
  

