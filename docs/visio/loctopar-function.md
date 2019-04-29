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
ms.openlocfilehash: 65a08837d7d026836ebc8d5e35938ea049d005e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439979"
---
# <a name="loctopar-function"></a>Função LOCTOPAR

Retorna um ponto transformado em coordenadas pai no sistema de coordenadas de destino.
  
## <a name="syntax"></a>Sintaxe

LOCTOPAR (* * *srcPoint* * *, * * *srcRef* * *, * * *dstRef* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _srcPoint_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> | Um ponto nas coordenadas locais no sistema de coordenadas de origem.  <br/> |
| _srcRef_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> | Uma referência a uma célula no objeto de origem.  <br/> |
| _dstRef_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> | Uma referência a uma célula no objeto de destino.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

Converte um ponto de coordenadas locais em uma forma de origem em coordenadas pai em uma forma de destino. Utilize a função LOCTOPAR para definir coordenadas pai em células, como PinX, PinY, BeginX e BeginY, em uma forma que esteja usando outro ponto de um outro sistema de coordenadas. 
  
Esta função funciona mesmo que as formas de origem e de destino estejam em grupos. Além disso, ajusta para rotação e inverte na transformação intermediária. 
  
As coordenadas de origem e de destino devem estar na mesma página. 
  
Se o destino for uma página que não tem um pai, o resultado será expresso em coordenadas locais da página. 
  
## <a name="example"></a>Exemplo

LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width) 
  
Converterá o pino local da forma associada à fórmula em coordenadas pai de Sheet.4. 
  

