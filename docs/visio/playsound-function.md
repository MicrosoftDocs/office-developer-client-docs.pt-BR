---
title: Função PLAYSOUND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
localization_priority: Normal
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: Reproduz um arquivo de som ou som do sistema.
ms.openlocfilehash: 752412aab6584d2b01235fe88644e3ec3fa5daee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435835"
---
# <a name="playsound-function"></a>Função PLAYSOUND

Reproduz um arquivo de som ou som do sistema. 
  
## <a name="syntax"></a>Sintaxe

PLAYSOUND(" ** *filename* ** "|" ** *alias* ** ", ** *isAlias* **, ** *beep* **, ** *synch* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _filename_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome do arquivo de som a ser executado.  <br/> |
| _alias_ <br/> |Obrigatório  <br/> |**String** <br/> | Um som de sistema representado por um alias.  <br/> |
| _isAlias_ <br/> |Obrigatório  <br/> |**Boolean** <br/> | Especifica se a expressão precedente é um alias ou um nome de arquivo; utilize um valor diferente de zero para especificar um alias.  <br/> |
| _beep_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Especifica se haverá um alarme sonoro do Microsoft Visio quando o som não puder ser reproduzido; utilize um número diferente de zero para o alarme sonoro.  <br/> |
| _synch_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Determina se o som será reproduzido de forma assíncrona (0) ou síncrona (1).  <br/> |
   
## <a name="remarks"></a>Comentários

Geralmente, você deve tocar sons de forma assíncrona para que o Visio possa continuar a processar enquanto o som estiver sendo tocado. Para criar cadeias de caracteres de vários sons juntos, execute-os de forma síncrona ou alguns deles poderão falhar. 
  
## <a name="example-1"></a>Exemplo 1

PLAYSOUND("chord.wav", 0, 0, 0)
  
Reproduz o arquivo de áudio wave chord.wav de forma assíncrona sem aviso sonoro.
  
## <a name="example-2"></a>Exemplo 2

PLAYSOUND("ExclamaçãodeSistema", 1, 0, 0)
  
Reproduz o som de exclamação de sistema de forma assíncrona sem aviso sonoro.
  

