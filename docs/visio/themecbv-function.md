---
title: Função THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Retorna um valor RGB ou um inteiro que representa um índice na paleta de cores do documento, onde a cor (número) passada como um argumento foi modificada pelo valor especificado tonalidade armazenado nas configurações do gradientes do tema ativo.
ms.openlocfilehash: 878da505a840234445d3e16d3b8a68e31eaf5fda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773141"
---
# <a name="themecbv-function"></a>Função THEMECBV

Retorna um valor RGB ou um inteiro que representa um índice na paleta de cores do documento, onde a cor (número) passada como um argumento foi modificada pelo valor especificado tonalidade armazenado nas configurações do gradientes do tema ativo. 
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **THEMECBV** ( _cor_, _gradient_stop_number_)
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**Número** <br/> |Um número representando um índice na paleta de cores do documento.  <br/> |
| _gradient_stop_number_ <br/> |Obrigatório  <br/> |**Número** <br/> |Parada de gradiente (tonalidade ou sombreamento) armazenada nas configurações do gradientes do tema ativo a ser aplicado à cor.  <br/> |
   
## <a name="return-value"></a>Valor retornado

 **Número**
  
## <a name="remarks"></a>Comentários

> [!NOTE]
> A função THEMECBV não faz nada à cor passada como um argumento se a propriedade QuickStyle que é atribuída à forma não tiver um preenchimento gradiente. 
  
As configurações de gradiente em um tema são uma série de paradas de gradiente numeradas que correspondem a um (tonalidade) "iluminação" ou "escurecimento" (sombra). Esses tons e matizes são aplicados a uma cor base para criar um efeito de gradiente de cores.
  
A função **THEMECBV** recebe uma entrada de cor e a cor de saídas depois que ele tiver sido modificado pela tonalidade ou o sombreamento da parada do gradiente especificado. Os matizes e tons vêm de definição do tema, se o estilo rápido atual contiver um preenchimento de gradiente. Se o estilo rápido ativo não especificar que um preenchimento gradual ou a forma estiver definida como Nenhum tema, esta fórmula simplesmente retorna a cor que é passada para o primeiro argumento. 
  
## <a name="example"></a>Exemplo

 `THEMECBV(FillForegnd, 5)`
  
Retorna a cor criada aplicando a tonalidade ou o sombreamento do quinto parada de gradiente do gradiente da cor especificada na célula **FillForegnd** . 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Retorna um sombreamento ou tonalidade de vermelho criada aplicando-a segunda parada de gradiente com uma cor base de vermelho.
  

