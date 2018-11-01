---
title: Desmarque o método - ActiveX Data Objects (ADO)
TOCTitle: Clear Method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 864c31a75514b4e8c56383672b196a4e62c4ec8f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876781"
---
# <a name="clear-method-ado"></a>Método Clear (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Remove todos os objetos **Error** da coleção **Errors**.

## <a name="syntax"></a>Sintaxe

*Erros*. Limpar

## <a name="remarks"></a>Comentários

Utilize o método **Clear** na coleção [Errors](errors-collection-ado.md) para remover todos os objetos [Error](error-object-ado.md) existentes da coleção. Quando ocorre um erro, o ADO limpa automaticamente a coleção **Errors** e a preenche com objetos **Error** com base no novo erro.

Algumas propriedades e métodos retornam avisos que aparecem como objetos **Error** na coleção **Errors** mas não suspendem a execução de um programa. Antes de chamar os métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) em um objeto [Recordset](recordset-object-ado.md); o método [Open](open-method-ado-connection.md) em um objeto [Connection](connection-object-ado.md); ou definir a propriedade [Filter](filter-property-ado.md) em um objeto **Recordset**, chame o método **Clear** na coleção **Errors**. Dessa forma, é possível ler a propriedade [Count](count-property-ado.md) da coleção **Errors** para testar os avisos retornados.

