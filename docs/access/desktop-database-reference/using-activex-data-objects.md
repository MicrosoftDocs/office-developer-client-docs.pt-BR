---
title: Usar ADO (ActiveX Data Objects)
TOCTitle: Use ActiveX Data Objects
description: O Microsoft Access oferece três modelos de objetos para uso em criação, manutenção e gerenciamento de seus bancos de dados do Access e seus dados relacionados usando o Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3b530db43a816e66b9fbef254984142aadf0b841
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719222"
---
# <a name="use-activex-data-objects"></a>Usar ADO (ActiveX Data Objects)

**Aplica-se a**: Access 2013, o Office 2013

O Microsoft Access oferece três modelos de objetos para uso em criação, manutenção e gerenciamento de seus bancos de dados do Access e seus dados relacionados usando o Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Microsoft ActiveX Data Objects (ADO)

O ADO contém os objetos necessários para criar, atualizar e excluir registros em uma determinada fonte de dados.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext. DDL e segurança (ADOX)

O ADOX fornece os objetos da Data Definition Language (DDL) necessários para criar um novo banco de dados e seus objetos contidos além dos objetos necessários para gerenciar a segurança.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>O Microsoft Jet and Replication objetos 2.5 library (JRO)

Porque os objetos ADO foram estruturados para funcionar com muitos bancos de dados, além dos bancos de dados do Microsoft Jet, a funcionalidade específica do Jet foi segmentada na biblioteca JRO.

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
(MDBs)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Crie conjuntos de registros.</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Edite propriedades de inicialização.</p></td>
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Suporte ANSI92 SQL.* * *</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Crie tabelas.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Crie um novo banco de dados.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Edite propriedades da tabela existente.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Crie relações entre tabelas.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Edite configurações de segurança.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Suporte para o atributo compactação dos dados da coluna.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Edite armazenado, básica modos de exibição ou consultas SQL.</p></td>
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
<td><p>Compactar/codifica banco de dados.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Atualize o cache.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>Torne o banco de dados replicável.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Criar réplicas de banco de dados.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Sincronize as réplicas.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Edite propriedades de banco de dados.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Crie propriedades de banco de dados personalizado.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Edite propriedades de coluna da tabela.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Disponível somente quando estiver trabalhando com bancos de dados do Microsoft Access (.mdb). As versões futuras do provedor do SQL poderão proporcionar essa funcionalidade nos projetos do Microsoft Access (.adp).

\*\* Disponível somente quando estiver trabalhando com projetos do Access.

\*\*\*Embora o mecanismo de banco de dados do Access oferece suporte algum ANSI 92 SQL, ele ainda não está totalmente compatível com ANSI92.

1 objeto usa **Conexão** ao banco de dados de referência.

Objeto de usos **catálogo** 2 ao banco de dados de referência.

Objeto de usos **réplica** 3 ao banco de dados de referência.

Objeto de usos **JetEngine** 4 ao banco de dados de referência.


> [!NOTE]
> Ao contrário do DAO, objetos ADO e ADOX podem executar as ações marcadas em bancos de dados que não sejam Jet desde que o provedor desses bancos de dados oferece suporte a essa ação.


