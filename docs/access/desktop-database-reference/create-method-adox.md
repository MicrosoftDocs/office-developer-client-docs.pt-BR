---
title: Método Create (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 866faae5d8c99258075a81f504fa9ce069f4690a
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949373"
---
# <a name="create-method-adox"></a>Método Create (ADOX)

**Aplica-se a**: Access 2013, o Office 2013

Cria um novo catálogo.

## <a name="syntax"></a>Sintaxe

*Catálogo*. Criar*ConnectString*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*ConnectString* |Um valor **String** usado para estabelecer conexão com a fonte de dados.|

## <a name="remarks"></a>Comentários

O método **Create** cria e abre uma nova [Conexão](connection-object-ado.md) do ADO com a fonte de dados especificada em *ConnectString*. Se for bem-sucedido, o novo objeto **Connection** será atribuído à propriedade [ActiveConnection](activeconnection-property-adox.md).

Ocorrerá um erro se o provedor não oferecer suporte para a criação de novos catálogos.

