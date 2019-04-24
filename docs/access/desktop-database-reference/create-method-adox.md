---
title: Método Create (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e98854665185d682b9049b000bf4b600040ba624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295419"
---
# <a name="create-method-adox"></a>Método Create (ADOX)

**Aplica-se ao:** Access 2013, Office 2013

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

