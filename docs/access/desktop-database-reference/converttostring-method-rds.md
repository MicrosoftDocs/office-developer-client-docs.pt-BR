---
title: Método ConvertToString (RDS)
TOCTitle: ConvertToString method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0accdb33aecacdb6bb6c51a3ec1a39d2edb08ead
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949443"
---
# <a name="converttostring-method-rds"></a>Método ConvertToString (RDS)

**Aplica-se a**: Access 2013, o Office 2013 

Converte um [Recordset](recordset-object-ado.md) em uma sequência MIME que representa os dados do conjunto de registros.

## <a name="syntax"></a>Sintaxe

*DataFactory*. ConvertToString (*Recordset*)

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*DataFactory* |Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).|
|*Recordset* |Uma variável de objeto que representa um objeto **Recordset**.|

## <a name="remarks"></a>Comentários

Com arquivos .asp, utilize **ConvertToString** para inserir o **Recordset** em uma página HTML gerada no servidor para transportá-la para um computador cliente.

**ConvertToString** primeiro carrega o **Recordset** nas tabelas de Serviço de Cursor e, em seguida, gera um fluxo no formato MIME.

No cliente, o Remote Data Service pode converter a sequência MIME de volta em um **Recordset** totalmente funcional. Isso funciona bem para tratar menos de 400 linhas de dados com não mais de 1024 bytes de largura por linha. Você não deve utilizá-lo para efetuar o streaming de dados BLOB e grandes conjuntos de resultado por HTTP. Nenhuma compactação em fio é executada na sequência, portanto conjuntos de dados muito grandes levarão um tempo considerável para transporte por HTTP quando comparados ao formato de tabela otimizada para fio definido e implementado pelo Remote Data Service como seu formato de protocolo de transporte nativo.

> [!NOTE]
> [!OBSERVAçãO] Se estiver utilizando Active Server Pages para inserir a sequência MIME resultante em uma página HTML cliente, esteja ciente de que as versões do VBScript anteriores à versão 2.0 limitam o tamanho da sequência a 32K. Se esse limite for excedido, será retornado um erro. Mantenha o escopo da consulta relativamente pequeno ao utilizar inserção de MIME utilizando arquivos .asp. Para corrigir isso, baixe a versão mais recente do VBScript na [Centro de Download da Microsoft](https://www.microsoft.com/download/default.aspx).


