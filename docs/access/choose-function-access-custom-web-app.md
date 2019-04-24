---
title: Função escolha (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Retorna o item no índice especificado a partir de uma lista de valores.
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282282"
---
# <a name="choose-function-access-custom-web-app"></a>Função escolha (aplicativo Web personalizado do Access)

Retorna o item no índice especificado a partir de uma lista de valores.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

**Escolha** (*IndexNumber*, *Value*, [*Value_n*]) 
  
A função **escolher** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *IndexNumber*  <br/> |Uma expressão de inteiro que representa um índice baseado em 1 na lista de itens que a segue.  <br/> |
| *Valor*  <br/> |Lista de valores de qualquer tipo de dados.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o *IndexNumber* fornecido não for um inteiro, o valor será convertido implicitamente em um inteiro. 
  
Se o valor do índice exceder os limites da matriz de valores, **escolha** retornará NULL. 
  

