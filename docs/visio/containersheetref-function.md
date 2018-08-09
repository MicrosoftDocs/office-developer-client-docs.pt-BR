---
title: Função CONTAINERSHEETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Retorna uma referência de planilha para o contêiner especificado que contém a forma.
ms.openlocfilehash: 6392b4c1a2652f1a831dc585c0be0f430a5ffe0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771603"
---
# <a name="containersheetref-function"></a>Função CONTAINERSHEETREF

Retorna uma referência de planilha para o contêiner especificado que contém a forma.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

CONTAINERSHEETREF (* * *índice* * * * * *[, categoria]* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _índice_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O índice baseado em 1 do contêiner. Consulte Comentários para obter mais informações.  <br/> |
| _category_ <br/> |Opcional  <br/> |**String** <br/> |A categoria do contêiner. Consulte Comentários para obter mais informações.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Referência do ShapeSheet
  
## <a name="remarks"></a>Comentários

O índice de um contêiner é calculado com base na ordem Z dos contêineres, de frente para trás.
  
 *Categorias* são cadeias de caracteres definidas pelo usuário que podem ser usados para categorizar as formas. Você pode definir categorias na célula User.msvShapeCategories na ShapeSheet de uma forma. Você pode definir várias categorias para uma forma, separando as categorias por ponto e vírgula. 
  
Se a forma não for membro de um contêiner ou não houver nenhum contêiner que corresponda tanto à categoria como ao número de índice especificado, CONTAINERSHEETREF retornará #REF!.
  
## <a name="example"></a>Exemplo

CONTAINERSHEETREF(1)!Height 
  
Retorna o valor na célula Height do contêiner que está mais à frente na página à qual a forma pertence. 
  

