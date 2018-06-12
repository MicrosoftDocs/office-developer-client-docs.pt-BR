---
title: Escolha a função (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Retorna o item no índice especificado de uma lista de valores.
ms.openlocfilehash: a6db959945bfcfc15993d3979cb9b2b3da0da904
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765066"
---
# <a name="choose-function-access-custom-web-app"></a>Escolha a função (aplicativo da web personalizado do Access)

Retorna o item no índice especificado de uma lista de valores.
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Syntax

**Escolha** (*Número_de_índice*, *valor*, [*Value_n*]) 
  
A função **Escolher** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Número_de_índice*  <br/> |Uma expressão de inteiro que representa um índice baseado em 1 para a lista dos itens depois dela.  <br/> |
| *Valor*  <br/> |Lista de valores de qualquer tipo de dados.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Se o fornecido *Número_de_índice* não for um inteiro, o valor implicitamente é convertido em um número inteiro. 
  
Se o valor de índice ultrapassar os limites da matriz de valores, **Escolher** retornará NULL. 
  

