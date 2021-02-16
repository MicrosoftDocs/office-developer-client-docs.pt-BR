---
title: Função CONTAINERSHEETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Retorna uma referência de planilha para o contêiner especificado que contém a forma.
ms.openlocfilehash: 473d8c0b81ecc568c1d4f3a3b3a885e1ceb4e00d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437263"
---
# <a name="containersheetref-function"></a>Função CONTAINERSHEETREF

Retorna uma referência de planilha para o contêiner especificado que contém a forma.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

CONTAINERSHEETREF(** *index* ** ** *[, category]* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _índice_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O índice baseado em 1 do contêiner. Consulte Comentários para obter mais informações.  <br/> |
| _category_ <br/> |Opcional  <br/> |**String** <br/> |A categoria do contêiner. Consulte Comentários para obter mais informações.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Referência do ShapeSheet
  
## <a name="remarks"></a>Comentários

O índice de um contêiner é calculado com base na ordem Z dos contêineres, de frente para trás.
  
 *As*  categorias são cadeias de caracteres definidas pelo usuário que você pode usar para categorizar formas. Você pode definir categorias na célula User.msvShapeCategories do ShapeSheet para uma forma. Pode também definir várias categorias para uma forma separando-as com ponto-e-vírgula. 
  
Se a forma não for membro de um contêiner ou não houver nenhum contêiner que corresponda tanto à categoria como ao número de índice especificado, CONTAINERSHEETREF retornará #REF!.
  
## <a name="example"></a>Exemplo

CONTAINERSHEETREF(1)! Altura 
  
Retorna o valor na célula Height do contêiner que está mais à frente na página à qual a forma pertence. 
  

