---
title: Objeto de Conexão (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bba06d593069051d2cc4f2e66b8cb91f36d920fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462765"
---
# <a name="connection-object-dao"></a>Objeto de Conexão (DAO)


**Aplica-se a**: Access 2013 | Office 2013


> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>



Um objeto **Connection** representa uma conexão com um banco de dados ODBC (apenas espaços de trabalho ODBCDirect).

## <a name="remarks"></a>Comentários

**Connection** é um objeto não persistente que representa uma conexão com um banco de dados remoto. O objeto **Connection** está disponível somente nos espaços de trabalho ODBCDirect (isto é, um objeto **Workspace** criado com a opção de tipo definida como **dbUseODBC**).


> [!NOTE]
> <P>[!OBSERVAçãO] O código gravado por versões anteriores do DAO pode continuar usando o objeto <STRONG>Database</STRONG> para obter compatibilidade com versões anteriores, mas se os novos recursos de um objeto <STRONG>Connection</STRONG> forem desejados, você deverá revisar o código para usar o objeto <STRONG>Connection</STRONG>. Para ajudar na conversão de código, será possível obter uma referência do objeto <STRONG>Connection</STRONG> a partir de um <STRONG>Database</STRONG>, lendo a propriedade <A href="database-connection-property-dao.md">Connection</A> do objeto <STRONG>Database</STRONG>. Por outro lado, você pode obter uma referência do objeto <STRONG>Database</STRONG> a partir da propriedade <STRONG>Database</STRONG> do objeto <STRONG>Connection</STRONG>.</P>


