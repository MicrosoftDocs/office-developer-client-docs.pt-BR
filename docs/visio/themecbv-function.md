---
title: Função THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Retorna um valor RGB ou um inteiro que representa um índice na paleta de cores do documento, onde a cor (número) passada como um argumento foi modificada pelo valor de tonalidade ou sombreamento especificado armazenado nas configurações de gradiente do tema ativo.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429135"
---
# <a name="themecbv-function"></a>Função THEMECBV

Retorna um valor RGB ou um inteiro que representa um índice na paleta de cores do documento, onde a cor (número) passada como um argumento foi modificada pelo valor de tonalidade ou sombreamento especificado armazenado nas configurações de gradiente do tema ativo. 
  
## <a name="version-information"></a>Informações sobre a versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **THEMECBV**( _cor_,  _gradient_stop_number_)
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**Número** <br/> |Um número que representa um índice na paleta de cores do documento.  <br/> |
| _gradient_stop_number_ <br/> |Obrigatório  <br/> |**Número** <br/> |A marca de gradiente (tonalidade ou sombreamento) armazenada nas configurações de gradiente do tema ativo a ser aplicada à cor.  <br/> |
   
## <a name="return-value"></a>Valor de retorno

 **Número**
  
## <a name="remarks"></a>Comentários

> [!NOTE]
> A função THEMECBV não faz nada com a cor passada como um argumento se o Estilo Rápido atribuído à forma não tiver um gradiente. 
  
As configurações de gradiente em um tema são uma série de paradas de gradiente numeradas que correspondem a uma "tonalidade" (tonalidade) ou "escurecer" (sombreamento). Esses tons e tonalidades são aplicados a uma cor base para criar um efeito de cor gradiente.
  
A **função THEMECBV** recebe uma entrada de cor e em saída a cor depois de ter sido modificada pela tonalidade ou sombreamento da parada de gradiente especificada. Os tons e tonalidades vêm da definição do tema, se o estilo rápido atual contiver um preenchimento de gradiente. Se o Estilo Rápido ativo não especificar um preenchimento de gradiente ou a forma estiver definida como Sem Tema, essa fórmula simplesmente retornará a cor passada para o primeiro argumento. 
  
## <a name="example"></a>Exemplo

 `THEMECBV(FillForegnd, 5)`
  
Retorna a cor criada aplicando a tonalidade ou sombreamento na quinta parada de gradiente do gradiente à cor especificada na **célula FillForegnd.** 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Retorna um sombreamento ou tonalidade de vermelho criado aplicando a segunda parada de gradiente a uma cor base de vermelho.
  

