---
title: Usar um domínio de aplicativo separado para evitar falhas
TOCTitle: Using a separate application domain to avoid crashing
ms:assetid: 7fc6d1e5-7032-47a9-826f-6b5d3b43fef9
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb623114(v=office.15)
ms:contentKeyID: 55119786
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b397fa2ad37102e12a3a0cf569e74323391b8e86
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407251"
---
# <a name="using-a-separate-application-domain-to-avoid-crashing"></a>Usar um domínio de aplicativo separado para evitar falhas

Suplementos gerenciados que implementam a interface **IDTExtensibility2** são carregados no mesmo domínio de aplicativo padrão. Quando um suplemento no domínio do aplicativo falha, ele pode causar falhas em outros suplementos no mesmo domínio de aplicativo.

Para contornar esse problema, você pode criar um shim para o suplemento, para que o suplemento possa ser carregado em seu próprio domínio de aplicativo. Um shim é uma biblioteca de vínculo dinâmico (DLL) não gerenciada. Quando você usa um shim, você p registra em vez do suplemento. O Outlook carrega o shim, que carrega o suplemento para o qual foi criado. Você deve criar e registrar um shim separado para cada suplemento. Para saber mais sobre o desenvolvimento de shims para suplementos gerenciados, confira [Isolar extensões do Office com o Assistente de Shims COM](https://go.microsoft.com/fwlink/?linkid=89109).

Outra alternativa para carregar seu suplemento no domínio de um aplicativo separado é desenvolver o suplemento usando ferramentas de desenvolvimento do Office no Visual Studio 2010 ou em uma versão posterior das Ferramentas de Desenvolvedor do Office para Visual Studio. Suplementos desenvolvidos por essas versões das Ferramentas de Desenvolvedor do Office para Visual Studio não implementam a interface IDTExtensibility2, mas usam a interface **IStartup**. Eles usam um carregador fornecido pelo Visual Studio, AddinLoader.dll, que funciona como um shim genérico. O Outlook procura no registro por suplementos criados com o Visual Studio. 

Quando o Outlook encontra esses suplementos, o Outlook inicia o AddinLoader.dll que, em seguida, inicia o tempo de execução do Visual Studio Tools para Office e retransmite o manifesto de aplicativo para ele. Em seguida, o tempo de execução do Visual Studio Tools for Office carrega cada suplemento em um domínio de aplicativo separado. Para mais informações sobre como o Visual Studio carrega um suplemento, confira [Arquitetura de suplementos ao nível de aplicativo](https://msdn.microsoft.com/library/bb386298\(v=office.15\)).
