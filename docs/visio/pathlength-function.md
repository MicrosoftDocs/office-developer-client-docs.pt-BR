---
title: Função PATHLENGTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Retorna o tamanho do caminho definido na seção Geometry especificada.
ms.openlocfilehash: e4f90c2bb886f54164bedab5f8d78fc528758414
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405846"
---
# <a name="pathlength-function"></a>Função PATHLENGTH

Retorna o tamanho do caminho definido na seção Geometry especificada.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

PATHLENGTH(** *seção* ** ** *[,segmento]* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**String** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _segmento_ <br/> |Opcional  <br/> |**Integer** <br/> |O segmento baseado em 1 do caminho a ser medido.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

 **Double**
  
## <a name="remarks"></a>Comentários

Se  _não_ existir  _seção ou_ segmento, o Microsoft Visio retornará #REF!. 
  
Se você incluir um  _valor_ de segmento, PATHLENGTH retornará apenas o comprimento desse segmento. 
  

