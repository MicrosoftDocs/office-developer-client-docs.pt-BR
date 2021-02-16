---
title: Função FIND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Localiza uma cadeia de caracteres de texto contida em outra cadeia de caracteres de texto e retorna a posição inicial da cadeia de caracteres de texto que você está procurando em relação à sua posição na cadeia de caracteres de texto que a contém.
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426573"
---
# <a name="find-function"></a>Função FIND

Localiza uma cadeia de caracteres de texto contida em outra cadeia de caracteres de texto e retorna a posição inicial da cadeia de caracteres de texto que você está procurando em relação à sua posição na cadeia de caracteres de texto que a contém.
  
## <a name="syntax"></a>Sintaxe

FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ ** *ignore_case* ** ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _find_text_ <br/> |Obrigatório  <br/> |**String** <br/> |A cadeia de caracteres de texto a ser localizada.  <br/> |
| _format_ <br/> |Obrigatório  <br/> |**String** <br/> |A cadeia de caracteres que contém o texto a ser localizado.  <br/> |
| _start_num_ <br/> |Opcional  <br/> |**Número** <br/> |O caractere para início da pesquisa. O primeiro caractere no  _within_text_ é 1. Se  _start_num_ está faltando, supõe-se que seja 1.  <br/> |
| _ignore_case_ <br/> |Opcional  <br/> |**Boolean** <br/> |Por padrão, a função FIND distingue maiúsculas e minúsculas. Para que a função FIND ignore maiúsculas e minúsculas, defina este argumento como TRUE.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
## <a name="remarks"></a>Comentários

Se vários valores correspondentes forem localizados, a função FIND retornará a posição inicial do primeiro valor correspondente na cadeia de caracteres. O  _find_text_ argumento não considera caracteres curinga. 
  
Se  _find_text_:
  
-  Está vazio (""), PROCURAR corresponde ao primeiro caractere na cadeia de caracteres de pesquisa (ou seja, o caractere numerado  _start_num_ ou 1). 
    
- Não aparece em  _within_text_, FIND retorna o #VALUE! valor de erro. 
    
Se  _start_num_:
  
- Não for maior que zero (0), PROCURAR retornará o #VALUE! valor de erro. 
    
- É maior do que o comprimento  _within_text_, FINDreturns o #VALUE! valor de erro. 
    
## <a name="example"></a>Exemplo

FIND ("2003","1º de janeiro de 2003") 
  
Retornará 12. 
  

