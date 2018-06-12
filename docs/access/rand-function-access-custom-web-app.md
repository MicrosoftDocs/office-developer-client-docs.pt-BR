---
title: Função RAND (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Retorna um número pseudo-aleatório entre 0 e 1.
ms.openlocfilehash: ed0f9991b2b1d9553d6d45524d6b1e4e5321ea7e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765210"
---
# <a name="rand-function-access-custom-web-app"></a>Função RAND (aplicativo da web personalizado do Access)

Retorna um número pseudo-aleatório entre 0 e 1.
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Syntax

 **Rand** ([ *Propagação* ]) 
  
A função **Rand** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Seed*  <br/> |Uma expressão de inteiro que retornará o valor de propagação. Se *propagar* não for especificado, um valor de propagação é atribuído aleatoriamente.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Chamadas repetitivas da função **Rand** com a mesma propagação retornam os mesmos resultados. 
  

