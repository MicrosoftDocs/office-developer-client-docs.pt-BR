---
title: Função PATHLENGTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Retorna o tamanho do caminho definido na seção Geometry especificada.
ms.openlocfilehash: 37cabbde9fc0782bc1fde46f3065d0c945c9dada
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772473"
---
# <a name="pathlength-function"></a>Função PATHLENGTH

Retorna o tamanho do caminho definido na seção Geometry especificada.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

PATHLENGTH (* * *seção* * * * * *[, segmento]* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**String** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _segmento_ <br/> |Opcional  <br/> |**Integer** <br/> |O segmento baseado em 1 do caminho a ser medido.  <br/> |
   
### <a name="return-value"></a>Valor retornado

 **Double**
  
## <a name="remarks"></a>Comentários

Se não existir _section_ nem _segment_ , o Microsoft Visio retornará #REF!. 
  
Se você incluir um valor _segment_ , PATHLENGTH retornará o tamanho desse segmento apenas. 
  

