---
title: Função LOC (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Assume um ponto definido nas coordenadas locais de uma forma e retorna o ponto equivalente expressado nas coordenadas locais da forma associada à fórmula.
ms.openlocfilehash: 4728e5f8301c6ef10ddb0c14b6c0868a7a48b2a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422422"
---
# <a name="loc-function-visioshapesheet"></a>Função LOC (VisioShapeSheet)

Assume um ponto definido nas coordenadas locais de uma forma e retorna o ponto equivalente expressado nas coordenadas locais da forma associada à fórmula. 
  
## <a name="syntax"></a>Sintaxe

LOC(** *ponto* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _point_ <br/> |Obrigatório  <br/> |**String** <br/> | Um ponto definido nas coordenadas locais de uma forma.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

As coordenadas locais são medidas do canto inferior esquerdo do retângulo de seleção da forma. Ambas as formas devem estar na mesma página.
  
## <a name="example"></a>Exemplo

LOC(PNT(Sheet.5! LocPinX, Sheet.5! LocPinY)) 
  
Nesta expressão, PNT converte um conjunto de coordenadas locais em Sheet.5 para um ponto. (Sheet.5 é uma outra forma na mesma página de desenho.) Em seguida, LOC converte esse ponto para um ponto equivalente no sistema de coordenadas locais da forma atual, em relação ao canto inferior esquerdo do retângulo de seleção da forma atual. 
  
O 5 em Sheet.5 é o número de identificação da forma, exibido na caixa de diálogo **Nome da Forma** (guia **Desenvolvedor**). 
  

