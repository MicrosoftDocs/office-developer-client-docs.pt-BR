---
title: 'Erro do servidor de Internet: acesso negado'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 885bdc14e5d5d346a17e018a509acf5b6c52108d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944876"
---
# <a name="internet-server-error-access-denied"></a>Erro do servidor de Internet: acesso negado


**Aplica-se a**: Access 2013, o Office 2013

Se você receber este erro, geralmente significa que o Microsoft Internet Information Services (IIS) retornou o seguinte status:

HTTP\_STATUS\_NEGADOS 401

Certifique-se de que os diretórios acessados pelo IIS têm as permissões adequadas. RDS podem se comunicar com um servidor de web IIS executando em qualquer um dos três modos de autenticação de senha: anônima, básica ou o desafio/resposta do NT (chamado de autenticação integrada do Windows no Windows 2000). Além disso, o servidor web deve ter permissões para o computador de origem de dados, caso se trate de um computador Windows NT/Windows 2000.

