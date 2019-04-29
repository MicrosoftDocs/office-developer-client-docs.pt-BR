---
title: Função DateAdd (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Retorna uma data especificada com o intervalo de números especificado (inteiro positivo ou negativo) adicionado a uma parte de data especificada da data.
ms.openlocfilehash: 7cfd68c4983eee22a5e542facd72ea083deb3184
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423199"
---
# <a name="dateadd-function-access-custom-web-app"></a>Função DateAdd (aplicativo Web personalizado do Access)

Retorna uma data especificada com o intervalo de números especificado (inteiro positivo ou negativo) adicionado a uma parte de data especificada da data.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**DateAdd** (*Datepart*, *número*, *Data*) 
  
A função **DateAdd** contém os argumentos a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *DatePart*  <br/> |A parte da *Data* à qual um número inteiro é adicionado. Consulte a seção comentários para obter a lista de configurações válidas.  <br/> |
| *Número*  <br/> |É uma expressão que pode ser resolvida como um inteiro que é adicionado a *datepart* de *Data* . Se você especificar um valor com fração decimal, a fração será truncada.  <br/> |
| *Date*  <br/> |Uma expressão que pode ser resolvida como um valor de data/hora. A expressão de argumento de *Data* , expressão de coluna, variável definida pelo usuário ou literal de cadeia de caracteres.  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir lista todos os argumentos de *datepart* válidos. 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**trimestre** <br/> |
|**Mês** <br/> |
|**DayOfYear** <br/> |
|**day** <br/> |
|**útil** <br/> |
|**hora** <br/> |
|**inclusões** <br/> |
|**secundária** <br/> |
|**milissegundo** <br/> |
   
## <a name="example"></a>Exemplo

A expressão a seguir calcula o último dia do mês atual.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

A expressão a seguir calcula o último dia do mês anterior.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


