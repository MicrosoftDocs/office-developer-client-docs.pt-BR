---
title: Função THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Retorna um valor RGB ou um inteiro que representa um índice na paleta de cores do documento, onde a cor (número) passada como um argumento foi modificada pelo valor de tonalidade ou sombreamento especificado, armazenado nas configurações de gradiente do tema ativo.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332260"
---
# <a name="themecbv-function"></a>Função THEMECBV

Retorna um valor RGB ou um inteiro que representa um índice na paleta de cores do documento, onde a cor (número) passada como um argumento foi modificada pelo valor de tonalidade ou sombreamento especificado, armazenado nas configurações de gradiente do tema ativo. 
  
## <a name="version-information"></a>Informações sobre a versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **THEMECBV** ( _Color_, _gradient_stop_number_)
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**Número** <br/> |Um número que representa um índice na paleta de cores do documento.  <br/> |
| _gradient_stop_number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O limite de gradiente (tonalidade ou sombreamento) armazenado nas configurações de gradiente do tema ativo a ser aplicado à cor.  <br/> |
   
## <a name="return-value"></a>Valor de retorno

 **Número**
  
## <a name="remarks"></a>Comentários

> [!NOTE]
> A função THEMECBV não fará nada com a cor passada como um argumento se o modo rápido atribuído à forma não tiver um gradiente. 
  
As configurações de gradiente em um tema são uma série de interrupções de gradiente numeradas que correspondem a uma "luminosidade" (tonalidade) ou "escurecer" (sombreamento). Esses tons e matizes são aplicados a uma cor de base para criar um efeito de cor de gradiente.
  
A função **THEMECBV** tem uma entrada de cor e gera a cor após ela ter sido modificada pela tonalidade ou sombra da parada de gradiente especificada. As tonalidades e graduais vêm da definição do tema, se o estilo rápido atual contiver um preenchimento gradual. Se o estilo rápido ativo não especificar um preenchimento de gradiente ou a forma for definida como nenhum tema, essa fórmula simplesmente retornará a cor que foi passada para o primeiro argumento. 
  
## <a name="example"></a>Exemplo

 `THEMECBV(FillForegnd, 5)`
  
Retorna a cor criada por meio da aplicação da tonalidade ou do sombreamento na quinta parada de gradiente para a cor especificada na célula **FillForegnd** . 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Retorna um sombreamento ou tonalidade de vermelho criado aplicando a segunda parada de gradiente a uma cor de base vermelha.
  

