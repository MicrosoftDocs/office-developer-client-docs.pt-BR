---
title: Função DOOLEVERB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
localization_priority: Normal
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: Executa um verbo para o objeto OLE.
ms.openlocfilehash: c339d03a00afdf7f777bb0624ddb8fa75f277e05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301488"
---
# <a name="dooleverb-function"></a>Função DOOLEVERB

Executa um verbo para o objeto OLE.
  
## <a name="syntax"></a>Sintaxe

DOOLEVERB ("* * *verbo* * *") 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _verbo_ <br/> |Obrigatório  <br/> |**String** <br/> |O verbo a ser executado.  <br/> |
   
## <a name="remarks"></a>Comentários

Em versões anteriores do Visio, essa função aparece como _DOOLEVERB. As versões 4.0 e posteriores do Visio aceitam os dois estilos. 
  
## <a name="example"></a>Exemplo

DOOLEVERB ("Editar")
  
Executa o programa de objeto OLE e exibe o objeto vinculado ou incorporado para que ele possa ser editado.
  

