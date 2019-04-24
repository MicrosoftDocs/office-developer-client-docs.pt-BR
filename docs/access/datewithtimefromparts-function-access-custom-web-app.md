---
title: Função DateWithTimeFromParts (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Retorna uma data e hora com base em um ano especificado, mês, dia e hora.
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282137"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>Função DateWithTimeFromParts (aplicativo Web personalizado do Access)

Retorna uma data e hora com base em um ano especificado, mês, dia e hora.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**DateWithTimeFromParts** (*Ano*, *mês*, *dia*, *hora*, *minuto*, *segundo*) 
  
A função **DateWithTimeFromParts** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Year*  <br/> |Expressão de inteiro que especifica um ano.  <br/> |
| *Month*  <br/> |Expressão de inteiro que especifica um mês.  <br/> |
| *Day*  <br/> |Expressão de inteiro que especifica um dia.  <br/> |
| *Hour*  <br/> |Expressão de inteiro especificando horas.  <br/> |
| *Minute*  <br/> |Expressão de inteiro especificando minutos.  <br/> |
| *Second*  <br/> |Expressão de inteiro especificando segundos.  <br/> |
   
## <a name="remarks"></a>Comentários

**DateWithTimeFromParts** retorna um valor de data/hora totalmente inicializado. Se os argumentos não forem válidos, um erro será gerado. Se os argumentos necessários forem nulos, NULL será retornado. 
  

