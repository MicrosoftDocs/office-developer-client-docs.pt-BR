---
title: Eventos WillChangeField e FieldChangeComplete (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fd952cc09f410752f3eb7b5963059f8d6ee7c2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302482"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>Eventos WillChangeField e FieldChangeComplete (ADO)

**Aplica-se ao:** Access 2013, Office 2013

O evento **WillChangeField** é chamado antes que uma operação pendente altere o valor de um ou mais objetos [Field](field-object-ado.md) em [Recordset](recordset-object-ado.md). O evento **FieldChangeComplete** é chamado depois que o valor de um ou mais objetos **Field** tiver sido alterado.

## <a name="syntax"></a>Sintaxe

WillChangeField *cFields*, *Fields*, *adStatus*, *pRecordset*

FieldChangeComplete *cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*cFields* |Um **Long** que indica o número de objetos **Field** em *Fields*.|
|*Fields* |Para **WillChangeField**, o parâmetro *Fields* é uma matriz de **Variants** que contém os objetos **Field** com os valores originais. <br/><br/>
Para **FieldChangeComplete**, o parâmetro *Fields* é uma matriz de **Variants** que contém os objetos **Field** com os valores alterados.|
|*pError* |Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Quando **WillChangeField** for chamado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida. Será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente. <br/><br/>Quando **FieldChangeComplete** for cancelado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida ou como **adStatusErrorsOccurred** se a operação tiver falhado. <br/><br/>Antes que **WillChangeField** seja retornado, configure esse parâmetro como **adStatusCancel** para solicitar o cancelamento da operação pendente. <br/><br/>Antes que **FieldChangeComplete** seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.|
|*pRecordset* |Um objeto **Recordset**. O **Recordset** para o qual esse evento ocorreu.|

## <a name="remarks"></a>Comentários

O evento **WillChangeField** ou **FieldChangeComplete** pode ocorrer ao definir a propriedade [Value](value-property-ado.md) e chamar o método [Update](update-method-ado.md) com os parâmetros de matriz do valor e campo.

