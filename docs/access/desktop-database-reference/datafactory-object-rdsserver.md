---
title: Objeto DataFactory (RDSServer)
TOCTitle: DataFactory Object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba705854fc27a18fd0d3d7a7c6fd7acdefb3830f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462228"
---
# <a name="datafactory-object-rdsserver"></a>Objeto DataFactory (RDSServer)


**Aplica-se a**: Access 2013 | Office 2013

Este objeto corporativo padrão do servidor implementa os métodos que fornecem acesso de leitura/gravação aos dados das fontes de dados especificadas para os aplicativos do cliente.

## <a name="remarks"></a>Comentários

O objeto **RDSServer.DataFactory** foi criado como um objeto Automation do servidor que recebe solicitações do cliente. Em uma implementação da Internet, reside em um servidor Web e é instanciado pelo componente ADISAPI. O objeto **RDSServer.DataFactory** fornece acesso de leitura e gravação às fontes de dados especificadas, mas não contém nenhuma validação ou regras comerciais lógicas.

Se você usar um método disponível em ambos os objetos **RDSServer.DataFactory** e [RDS.DataControl](datacontrol-object-rds.md), o RDS usará a versão **RDS.DataControl** por padrão. O padrão adotará um cenário de programação básico, no qual o **RDSServer.DataFactory** servirá como um objeto corporativo genérico do servidor.

Se você quiser que o aplicativo da Web trate o processamento de tarefas específicas do servidor, substitua o **RDSServer.DataFactory** por um objeto corporativo personalizado.

Crie os objetos corporativos do servidor que chamam os métodos **RDSServer.DataFactory**, como [Query](query-method-rds.md) e [CreateRecordset](createrecordset-method-rds.md). Isso será útil, caso você queira adicionar funcionalidade aos objetos corporativos, mas tire proveito das tecnologias RDS existentes.

A ID de classe do objeto **RDSServer.DataFactory** é 9381D8F5-0288-11D0-9501-00AA00B911A5.

