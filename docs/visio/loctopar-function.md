---
title: Função LOCTOPAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
localization_priority: Normal
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: Retorna um ponto transformado em coordenadas pai no sistema de coordenadas de destino.
ms.openlocfilehash: 7d882ec34de93db2828fc751f99d87fc3e961d64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772305"
---
# <a name="loctopar-function"></a>Função LOCTOPAR

Retorna um ponto transformado em coordenadas pai no sistema de coordenadas de destino.
  
## <a name="syntax"></a>Sintaxe

LOCTOPAR (* * *srcPoint* * *, * * *srcRef* * *, * * *dstRef* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _srcPoint_ <br/> |Obrigatório  <br/> |**String** <br/> | Um ponto nas coordenadas locais no sistema de coordenadas de origem.  <br/> |
| _srcRef_ <br/> |Obrigatório  <br/> |**String** <br/> | Uma referência a uma célula no objeto de origem.  <br/> |
| _dstRef_ <br/> |Obrigatório  <br/> |**String** <br/> | Uma referência a uma célula no objeto de destino.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

Converte um ponto de coordenadas locais em uma forma de origem em coordenadas pai em uma forma de destino. Utilize a função LOCTOPAR para definir coordenadas pai em células, como PinX, PinY, BeginX e BeginY, em uma forma que esteja usando outro ponto de um outro sistema de coordenadas. 
  
Esta função funciona mesmo que as formas de origem e de destino estejam em grupos. Além disso, ajusta para rotação e inverte na transformação intermediária. 
  
As coordenadas de origem e de destino devem estar na mesma página. 
  
Se o destino for uma página que não tem um pai, o resultado será expresso em coordenadas locais da página. 
  
## <a name="example"></a>Exemplo

LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width) 
  
Converterá o pino local da forma associada à fórmula em coordenadas pai de Sheet.4. 
  

