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

Find (* * *texto_procurado* * *, * * *no_texto* * *, [* * *Núm_inicial* * *], [* * *ignore_case* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Texto_procurado_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |A cadeia de caracteres de texto a ser localizada.  <br/> |
| _format_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |A cadeia de caracteres que contém o texto a ser localizado.  <br/> |
| _núm_inicial_ <br/> |Opcional  <br/> |**Número** <br/> |O caractere para início da pesquisa. O primeiro caractere em _no_texto_ é 1. Se _Núm_inicial_ estiver faltando, será considerado 1.  <br/> |
| _ignore_case_ <br/> |Opcional  <br/> |**Boolean** <br/> |Por padrão, a função FIND distingue maiúsculas e minúsculas. Para que a função FIND ignore maiúsculas e minúsculas, defina este argumento como TRUE.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
## <a name="remarks"></a>Comentários

Se vários valores correspondentes forem localizados, a função FIND retornará a posição inicial do primeiro valor correspondente na cadeia de caracteres. O argumento _texto_procurado_ não considera nenhum caractere como curingas. 
  
Se _texto_procurado_:
  
-  Estiver vazio (""), FIND corresponde ao primeiro caractere na cadeia de caracteres de pesquisa (ou seja, o caractere numerado _Núm_inicial_ ou 1). 
    
- Não aparecer em _no_texto_, localizar retorna o #VALUE! valor de erro. 
    
Se _Núm_inicial_:
  
- Não é maior que zero (0), FIND retorna o #VALUE! valor de erro. 
    
- É maior que o comprimento de _no_texto_, FINDreturns o #VALUE! valor de erro. 
    
## <a name="example"></a>Exemplo

FIND ("2003","1º de janeiro de 2003") 
  
Retornará 12. 
  

