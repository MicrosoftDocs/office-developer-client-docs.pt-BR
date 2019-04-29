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
ms.openlocfilehash: f08feb6137c3022027d19b45f06285fb8b6441a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427483"
---
# <a name="loctoloc-function"></a>Função LOCTOLOC

Retorna um ponto transformado em coordenadas locais no sistema de coordenadas de destino.
  
## <a name="syntax"></a>Sintaxe

LOCTOLOC (* * *srcPoint* * *, * * *srcRef* * *, * * *dstRef* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _srcPoint_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> | Um ponto nas coordenadas locais no sistema de coordenadas de origem.  <br/> |
| _srcRef_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> | Uma referência a uma célula no objeto de origem.  <br/> |
| _dstRef_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> | Uma referência a uma célula no objeto de destino.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

A função LOCTOLOC converte um ponto de coordenadas locais de uma forma de origem em coordenadas locais de uma forma de destino. Utilize essa função para criar uma forma, por exemplo, um ponto de um outro espaço de coordenadas. É possível também usar essa função para transformar um ponto local em coordenadas de páginas ou vice-versa.
  
Esta função funciona mesmo que as formas de origem e de destino estejam em grupos. Além disso, ajusta para rotação e inverte na transformação intermediária.
  
As coordenadas de origem e de destino devem estar na mesma página.
  
## <a name="example"></a>Exemplo

A fórmula a seguir converte o pino local da forma associada com a fórmula em um ponto na página.
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


