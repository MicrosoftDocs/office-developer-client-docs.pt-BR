---
title: Função HASCATEGORY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Retornará TRUE se a cadeia de caracteres especificada for encontrada na lista de categorias da forma.
ms.openlocfilehash: 902819f981b53aed96695e181ab556d3841d97c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360162"
---
# <a name="hascategory-function"></a>Método HASCATEGORY

Retornará TRUE se a cadeia de caracteres especificada for encontrada na lista de categorias da forma.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

HASCATEGORY (* * *categoria* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Categorias_ <br/> |Obrigatório  <br/> |**String** <br/> |A categoria a ser procurada.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

 **Boolean**
  
## <a name="remarks"></a>Comentários

 As *categorias* são cadeias de caracteres definidas pelo usuário que você pode usar para categorizar formas. Você pode definir categorias na célula User.msvShapeCategories do ShapeSheet para uma forma. Pode também definir várias categorias para uma forma separando-as com ponto-e-vírgula. 
  

