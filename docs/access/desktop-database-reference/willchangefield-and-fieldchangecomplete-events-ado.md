---
title: Eventos WillChangeField e FieldChangeComplete (ADO)
TOCTitle: WillChangeField and FieldChangeComplete Events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa26ff85bfb3a2b5666b98ea6ab6b30e689b5c2b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872687"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>Eventos WillChangeField e FieldChangeComplete (ADO)


**Aplica-se a**: Access 2013, o Office 2013

O evento **WillChangeField** é chamado antes que uma operação pendente altere o valor de um ou mais objetos [Field](field-object-ado.md) em [Recordset](recordset-object-ado.md). O evento **FieldChangeComplete** é chamado depois que o valor de um ou mais objetos **Field** tiver sido alterado.

## <a name="syntax"></a>Sintaxe

De*cFields*, *campos*, de WillChangeField *adStatus*, *pRecordset*

FieldChangeComplete*cFields*, *campos*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parâmetros

  - *cFields*

  - Um **Long** que indica o número de objetos **Field** em *Fields*.

  - *Fields*

  - Para **WillChangeField**, o parâmetro *campos* é uma matriz de **variantes** que contém os objetos **Field** com os valores originais.  
      
    Para **FieldChangeComplete**, o parâmetro *campos* é uma matriz de **variantes** que contém os objetos **Field** com os valores alterados.

  - *pError*

  - Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Quando **WillChangeField** for chamado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida. Será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente.
    
    Quando **FieldChangeComplete** for cancelado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida ou como **adStatusErrorsOccurred** se a operação tiver falhado.
    
    Antes que **WillChangeField** seja retornado, configure esse parâmetro como **adStatusCancel** para solicitar o cancelamento da operação pendente.
    
    Antes que **FieldChangeComplete** seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.

  - *pRecordset*

  - Um objeto **Recordset**. O **Recordset** para o qual esse evento ocorreu.

## <a name="remarks"></a>Comentários

O evento **WillChangeField** ou **FieldChangeComplete** pode ocorrer ao definir a propriedade [Value](value-property-ado.md) e chamar o método [Update](update-method-ado.md) com os parâmetros de matriz do valor e campo.

