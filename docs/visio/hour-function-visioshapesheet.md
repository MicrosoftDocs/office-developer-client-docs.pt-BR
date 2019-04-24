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
description: Retorna um inteiro, de 0 a 23, representando a hora do dia de DateTime ou expressão.
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329964"
---
# <a name="hour-function-visioshapesheet"></a>Função HOUR (VisioShapeSheet)

Retorna um inteiro, de 0 a 23, representando a hora do dia de _DateTime_ ou _expressão_.
  
## <a name="syntax"></a>Sintaxe

HOUR ("* * *DateTime* * *" | * * *expressão* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> | Uma cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**Vai** <br/> |Uma expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> | Um identificador de local a ser utilizado na avaliação de uma data e hora não-locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
## <a name="remarks"></a>Comentários

O componente de data em *DateTime* e *expression* é Descartado. 
  
Não é feito nenhum arredondamento. Se o *DateTime* estiver faltando ou não puder ser convertido em um resultado válido, a função retornará um erro. 
  
O valor retornado é formatado de acordo com o estilo de hora definido pelas Configurações Regionais atuais do sistema. 
  
A função HOUR também aceita um valor de número único para *expressão* em que a parte decimal do resultado representa a fração de um dia desde a meia-noite. 
  
## <a name="example-1"></a>Exemplo 1

HORA ("15:45")
  
Retornará 15.
  
## <a name="example-2"></a>Exemplo 2

HOUR("30 de maio de 1997 15:45:24")
  
Retornará 15.
  
## <a name="example-3"></a>Exemplo 3

HORA (0,5)
  
Retornará 12.
  
## <a name="example-4"></a>Exemplo 4

HORA ("5/30/1997")
  
Retornará 0.
  

