---
title: Método Create (ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cffaa8fb924d2fd272300c77fc5a9c3dc0b239db
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464774"
---
# <a name="create-method-adox"></a>Método Create (ADOX)


**Aplica-se a**: Access 2013 | Office 2013


Cria um novo catálogo.

## <a name="syntax"></a>Sintaxe

*Catálogo*. Criar*ConnectString*

## <a name="parameters"></a>Parâmetros

  - *ConnectString*

  - Um valor **String** usado para estabelecer conexão com a fonte de dados.

## <a name="remarks"></a>Comentários

O método **Create** cria e abre uma nova [Conexão](connection-object-ado.md) do ADO com a fonte de dados especificada em *ConnectString*. Se for bem-sucedido, o novo objeto **Connection** será atribuído à propriedade [ActiveConnection](activeconnection-property-adox.md).

Ocorrerá um erro se o provedor não oferecer suporte para a criação de novos catálogos.

