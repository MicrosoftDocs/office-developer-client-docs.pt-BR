---
title: Usar ADO (ActiveX Data Objects)
TOCTitle: Use ActiveX Data Objects
description: O Microsoft Access fornece três modelos de objeto a ser usado na criação, manutenção e gerenciamento dos bancos de dados do Access e seus dados relacionados usando o Visual Basic.
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312737"
---
# <a name="use-activex-data-objects"></a>Usar ADO (ActiveX Data Objects)

**Aplica-se ao:** Access 2013, Office 2013

O Microsoft Access fornece três modelos de objeto a ser usado na criação, manutenção e gerenciamento dos bancos de dados do Access e seus dados relacionados usando o Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Microsoft ActiveX Data Objects (ADO)

O ADO contém os objetos necessários para criar, atualizar e excluir registros em uma determinada fonte de dados.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Ext. do Microsoft ADO para DDL e segurança (ADOX)

O ADOX fornece os objetos DDL (Data Definition Language) necessários para criar um novo banco de dados e seus objetos contidos, além dos objetos necessários para gerenciar a segurança.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Biblioteca do Microsoft Jet and Replication Objects 2.5 (JRO)

Como os objetos do ADO foram projetados para funcionar com muitos bancos de dados além dos bancos de dados do Microsoft Jet, a funcionalidade específica do Jet foi dividida na biblioteca JRO.

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
(somente MDBs)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Criar Recordsets.</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar propriedades de Inicialização.</p></td>
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Suporte a ANSI92 SQL.***</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Criar tabelas.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Criar novo banco de dados.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar propriedades de tabela existentes.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Criar relações de tabela.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar configurações de segurança.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Suporte para o atributo Compression para dados de coluna.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar consultas SQL ou exibições básicas armazenadas.</p></td>
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
<td><p>Banco de dados compacta/codificado.</p></td>
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
<td><p>Tornar o banco de dados relicável.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Faça réplicas de banco de dados.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Sincronizar réplicas.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Editar propriedades do banco de dados.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Criar propriedades de banco de dados personalizadas.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar propriedades de coluna de tabela.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Disponível somente quando estiver trabalhando com bancos de dados do Microsoft Access (.mdb). As versões futuras do provedor do SQL poderão proporcionar essa funcionalidade nos projetos do Microsoft Access (.adp).

\*\* Disponível somente quando estiver trabalhando com projetos do Access.

\*\*\* Embora o mecanismo de banco de dados do Access suporte algum SQL ANSI 92, ele ainda não é totalmente compatível com ANSI92.

1 Usa o **objeto Connection** para fazer referência ao banco de dados.

2 Usa o **objeto Catalog** para fazer referência ao banco de dados.

3 Usa o **objeto Replica** para fazer referência ao banco de dados.

4 Usa **o objeto JetEngine** para fazer referência ao banco de dados.


> [!NOTE]
> Ao contrário do DAO, os objetos do ADO e do ADOX podem executar as ações marcadas em bancos de dados diferentes do Jet, desde que o provedor desses bancos de dados suporte essa ação.


