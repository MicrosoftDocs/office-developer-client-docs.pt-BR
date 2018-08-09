---
title: Função HOUR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Retorna um número inteiro, de 0 a 23, representando a hora do dia de datetime ou expression.
ms.openlocfilehash: 9cfe8c88a4a4d73be23b2ac230b0cfabc955c004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772031"
---
# <a name="hour-function-visioshapesheet"></a>Função HOUR (VisioShapeSheet)

Retorna um número inteiro, de 0 a 23, representando a hora do dia de _datetime_ ou _expression_.
  
## <a name="syntax"></a>Sintaxe

HORA ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> | Uma cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**Varia** <br/> |Uma expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> | Um identificador de local a ser utilizado na avaliação de uma data e hora não-locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
## <a name="remarks"></a>Comentários

O componente de data em *datetime* e *expression* é desconsiderado. 
  
É feito nenhum arredondamento. Se a *datetime* estiver faltando ou não puder ser convertida para um resultado válido, a função retornará um erro. 
  
O valor retornado é formatado de acordo com o estilo de hora definido pelas Configurações Regionais atuais do sistema. 
  
A função HOUR também aceita um valor de número único para *expression* em que a parte decimal do resultado representa a fração de um dia desde a meia-noite. 
  
## <a name="example-1"></a>Exemplo 1

HOUR("15:45")
  
Retornará 15.
  
## <a name="example-2"></a>Exemplo 2

HOUR("30 de maio de 1997 15:45:24")
  
Retornará 15.
  
## <a name="example-3"></a>Exemplo 3

HOUR(0.5)
  
Retornará 12.
  
## <a name="example-4"></a>Exemplo 4

HOUR("30/05/1997")
  
Retornará 0.
  

