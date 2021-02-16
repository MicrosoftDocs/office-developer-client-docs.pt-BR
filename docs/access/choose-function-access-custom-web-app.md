---
title: Função Choose (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Retorna o item no índice especificado de uma lista de valores.
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414113"
---
# <a name="choose-function-access-custom-web-app"></a>Função Choose (aplicativo Web personalizado do Access)

Retorna o item no índice especificado de uma lista de valores.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

**Choose** (*IndexNumber*, *Value*, [*Value_n*]) 
  
A **função** Escolher contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *IndexNumber*  <br/> |Uma expressão inteira que representa um índice baseado em 1 na lista dos itens que o seguem.  <br/> |
| *Valor*  <br/> |Lista de valores de qualquer tipo de dados.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o  *IndexNumber fornecido*  não for um inteiro, o valor será implicitamente convertido em um inteiro. 
  
Se o valor do índice exceder os limites da matriz de valores, **Choose** retornará NULL. 
  

