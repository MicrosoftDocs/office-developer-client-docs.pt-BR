---
title: Função GUARD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
localization_priority: Normal
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: Protege a expressão contra exclusão e alteração por ações executadas na janela de desenho, por exemplo, mover, dimensionamento, agrupar ou desagrupar as formas.
ms.openlocfilehash: fd5fcfbe11eb054dfa625834640c0280cae96c3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771985"
---
# <a name="guard-function"></a>Função GUARD

Protege a *expressão* contra exclusão e alteração por ações executadas na janela de desenho, por exemplo, mover, dimensionamento, agrupar ou desagrupar as formas. 
  
## <a name="syntax"></a>Sintaxe

GUARD (* * *expressão* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor.  <br/> |
   
## <a name="remarks"></a>Comentários

As células normalmente afetadas pela função GUARD são Width, Height, PinX e PinY. 
  
Proteger uma fórmula em qualquer célula evita que o valor da célula seja alterado por ações executadas na janela de desenho. No entanto, uma ação na janela de desenho pode afetar diversas células e cada uma dessas células deve estar protegida caso você deseje evitar alterações inesperadas na aparência da forma. 
  
## <a name="example"></a>Exemplo

GUARD(TEXTWIDTH(TheText) + 0,5 pol.) 
  
Esta expressão na célula Width de uma seção Shape Transform de uma forma impede que a expressão (TEXTWIDTH(TheText) + 0,5 pol.) seja substituída por outro valor quando a largura da forma for alterada na janela de desenho. TheText é uma célula disparada quando a composição do texto da forma associada é alterada. 
  

