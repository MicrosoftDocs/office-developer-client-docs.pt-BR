---
title: Função LOCTOLOC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251586
localization_priority: Normal
ms.assetid: 1f09482a-0b1b-1bef-bc23-7f7793c4c65f
description: Retorna um ponto transformado em coordenadas locais no sistema de coordenadas de destino.
ms.openlocfilehash: 444200801ebd984fb735b95de6d58d35e5160d1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772296"
---
# <a name="loctoloc-function"></a>Função LOCTOLOC

Retorna um ponto transformado em coordenadas locais no sistema de coordenadas de destino.
  
## <a name="syntax"></a>Sintaxe

LOCTOLOC (* * *srcPoint* * *, * * *srcRef* * *, * * *dstRef* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _srcPoint_ <br/> |Obrigatório  <br/> |**String** <br/> | Um ponto nas coordenadas locais no sistema de coordenadas de origem.  <br/> |
| _srcRef_ <br/> |Obrigatório  <br/> |**String** <br/> | Uma referência a uma célula no objeto de origem.  <br/> |
| _dstRef_ <br/> |Obrigatório  <br/> |**String** <br/> | Uma referência a uma célula no objeto de destino.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

A função LOCTOLOC converte um ponto de coordenadas locais de uma forma de origem em coordenadas locais de uma forma de destino. Utilize essa função para criar uma forma, por exemplo, um ponto de um outro espaço de coordenadas. É possível também usar essa função para transformar um ponto local em coordenadas de páginas ou vice-versa.
  
Esta função funciona mesmo que as formas de origem e de destino estejam em grupos. Além disso, ajusta para rotação e inverte na transformação intermediária.
  
As coordenadas de origem e de destino devem estar na mesma página.
  
## <a name="example"></a>Exemplo

A fórmula a seguir converte o pino local da forma associada com a fórmula em um ponto na página.
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


