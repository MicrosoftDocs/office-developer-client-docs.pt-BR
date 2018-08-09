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
ms.openlocfilehash: a7786c3ef2b4039e288596ed367083a4ed3a6c13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771753"
---
# <a name="dooleverb-function"></a>Função DOOLEVERB

Executa um verbo para o objeto OLE.
  
## <a name="syntax"></a>Sintaxe

DOOLEVERB ("* * *verbo* * *") 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _"verbo"_ <br/> |Obrigatório  <br/> |**String** <br/> |O verbo a ser executado.  <br/> |
   
## <a name="remarks"></a>Comentários

Em versões anteriores do Visio, essa função aparece como _DOOLEVERB. As versões 4.0 e posteriores do Visio aceitam os dois estilos. 
  
## <a name="example"></a>Exemplo

DOOLEVERB("editar")
  
Executa o programa de objeto OLE e exibe o objeto vinculado ou incorporado para que ele possa ser editado.
  

