---
title: Usando objetos de dados ActiveX
TOCTitle: Using ActiveX Data Objects
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1f7c57ca785e115e9278145921bf50e8afe870ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463091"
---
# <a name="using-activex-data-objects"></a>Usando objetos de dados ActiveX


**Aplica-se a**: Access 2013 | Office 2013

O Microsoft Access oferece três modelos de objetos para uso em criação, manutenção e gerenciamento de bancos de dados do Access e seus dados relacionados através do Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Microsoft ActiveX Data Objects (ADO)

O ADO contém os objetos necessários para criar, atualizar e excluir registros em uma determinada fonte de dados.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>O Microsoft ADO Ext. for DDL and Security (ADOX)

O ADOX fornece os objetos da Data Definition Language (DDL) necessários para a criação de novos bancos de dados e seus objetos contidos além dos objetos necessários para o gerenciamento da segurança.

**O Microsoft Jet and Replication Objects 2.5 Library (JRO)**

Como os objetos do ADO foram estruturados para funcionar com muitos bancos de dados além dos bancos de dados do Microsoft Jet, a funcionalidade específica do Jet foi segmentada na biblioteca JRO.

A tabela a seguir lista a funcionalidade fornecida por cada um deles em relação ao DAO.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Funcionalidade</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
(MDB do somente)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Criar conjuntos de registros</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Propriedades Edit Startup</p></td>
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Suporte a SQL ANSI92 ***</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Criar tabelas</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Criar novo banco de dados</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Propriedades Edit Existing Table</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Criar relações entre tabelas</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar configurações de segurança</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Suporte para o atributo Compactação dos dados da coluna</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar modos de exibição ou consultas SQL básicas armazenadas</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Criar consultas permanentes que são acessíveis somente através de código.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Criar consultas acessíveis através de contêiner/IU do banco de dados e código.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Compactar/Codificar banco de dados</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Atualizar cache</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>Criar banco de dados replicável</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Criar réplicas de banco de dados</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Sincronizar réplicas</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Propriedades Edit Database</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Criar propriedades de banco de dados personalizadas</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar propriedades da coluna da tabela</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Disponível somente quando estiver trabalhando com bancos de dados do Microsoft Access (.mdb). As versões futuras do provedor do SQL poderão proporcionar essa funcionalidade nos projetos do Microsoft Access (.adp).

\*\* Disponível somente quando estiver trabalhando com projetos do Access.

\*\*\* Embora o mecanismo do banco de dados do Access ofereça suporte parcial a SQL ANSI92, ele ainda não é totalmente compatível.

1Usa o objeto **Connection** para fazer referência ao banco de dados.

2Usa o objeto **Catalog** para fazer referência ao banco de dados.

3Usa o objeto **Replica** para fazer referência ao banco de dados.

4Usa o objeto **JetEngine** para fazer referência ao banco de dados.


> [!NOTE]
> <P>[!OBSERVAçãO] Ao contrário do DAO, os objetos do ADO e ADOX podem executar as ações marcadas em bancos de dados que não sejam Jet desde que o provedor desses bancos de dados ofereça suporte a essa ação.</P>


