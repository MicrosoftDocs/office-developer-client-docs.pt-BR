---
title: Função DateWithTimeFromParts (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Retorna uma Data e Hora com base em um ano, mês, dia e hora especificados.
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422086"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>Função DateWithTimeFromParts (aplicativo Web personalizado do Access)

Retorna uma Data e Hora com base em um ano, mês, dia e hora especificados.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**DateWithTimeFromParts** (*Ano*, *Mês*, *Dia*, *Hora*, *Minuto*, *Segundo*) 
  
A **função DateWithTimeFromParts** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Year*  <br/> |Expressão inteira especificando um ano.  <br/> |
| *Month*  <br/> |Expressão inteira especificando um mês.  <br/> |
| *Day*  <br/> |Expressão inteira especificando um dia.  <br/> |
| *Hour*  <br/> |Expressão inteira especificando horas.  <br/> |
| *Minute*  <br/> |Expressão inteira especificando minutos.  <br/> |
| *Second*  <br/> |Expressão inteira especificando segundos.  <br/> |
   
## <a name="remarks"></a>Comentários

**DateWithTimeFromParts** retorna um valor de Data/Hora totalmente inicializado. Se os argumentos não são válidos, um erro é gerado. Se os argumentos necessários são Nulos, Null é retornado. 
  

