---
title: Propriedade canônica PidTagFolderWebViewInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316307"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>Propriedade canônica PidTagFolderWebViewInfo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a URL da home page de uma pasta no Microsoft Outlook. Essa propriedade contém um fluxo binário chamado **WebViewPersistenceObject**.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Identificador:  <br/> |0x36DF  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Pasta MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Uma URL da home page pode ser especificada para qualquer pasta do Outlook. Essas informações podem ser acessadas no Outlook a partir da guia **Página** Inicial da caixa de diálogo Propriedades de uma pasta. 
  
Dependendo de certas configurações de política, a home page poderá ser ignorada pelo Outlook se o armazenamento MAPI que contém essa pasta não relatar MSCAP_SECURE_FOLDER_HOMEPAGES em sua implementação [IMSCapabilities::GetCapabilities.](pidtagfolderwebviewinfo-cannonical-property.md) 
  
Tanto a **pasta Outlook Today** quanto uma pasta pública podem ter URLs da página inicial. No **entanto, a pasta Outlook Today** usa um mecanismo diferente para gerenciar sua URL da home page; esse mecanismo não é abordado neste tópico. Uma pasta pública também pode ter uma URL da home page definida que seja específica para um usuário. No entanto, essa funcionalidade não está descrita neste tópico. 
  
O valor dessa propriedade é um fluxo binário chamado **WebViewPersistenceObject**.
  
### <a name="webviewpersistenceobject-stream-structure"></a>Estrutura de Fluxo de WebViewPersistenceObject

A **estrutura de fluxo WebViewPersistenceObject** contém informações sobre uma URL da home page para uma pasta. 
  
Os elementos de dados nessa estrutura são armazenados em ordem de byte little-endian, imediatamente após um ao outro na seguinte ordem especificada. 
  
> [!NOTE]
> A descrição a seguir pode não listar todos os valores de campo suportados pelo Outlook; portanto, quando seu código lê um fluxo existente, alguns sinalizadores que não estão listados aqui também podem ser encontrados. No entanto, você pode usar essa descrição para criar de forma programática valores para a propriedade **PidTagFolderWebViewInfo** que o Outlook compreenderá. 
  
 _dwVersion_
  
> DWORD (4 bytes). A versão do formato da estrutura. A partir do Microsoft Office Outlook 2007, o único valor com suporte para esse campo é o seguinte.
    
|**Value name**|**Valor**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 bytes). O tipo das informações da home page. A partir do Microsoft Office Outlook 2007, o único valor com suporte para esse campo é o seguinte.
    
|**Value name**|**Valor**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 bytes). Uma combinação de zero ou mais sinalizadores cujos valores e significados estão listados na tabela a seguir.
    
|Nome do sinalizador****|****Valor****|****Descrição****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |Por **padrão, a** caixa de seleção Mostrar home page dessa pasta foi marcada na guia **Home Page** da caixa de diálogo Propriedades de uma pasta.  <br/> |
   
 _dwUnused[7]_
  
> Uma matriz de sete elementos DWORD (total de 28 bytes). Não éusado.
    
cbData
  
> Um ULONG (4 bytes). O tamanho, em bytes, do _elemento de dados wzURL._ 
    
 _wzURL_
  
> Uma matriz de elementos WCHAR. A representação UTF-16 da cadeia de caracteres da URL da página inicial terminada por zero.
    
### <a name="webviewpersistenceobject-stream-sample"></a>Exemplo de fluxo de WebViewPersistenceObject

Esta seção descreve um exemplo de um **fluxo WebViewPersistenceObject.** O fluxo especifica a URL da página inicial " https://www.microsoft.com ". 
  
 **Despejo de dados**
  
A seguir está um despejo de dados do fluxo, como seria exibido em um editor binário.
  
|**Deslocamento de fluxo**|**Bytes de dados**|**Dados ASCII**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
A seguir está uma análise dos dados de amostra para o **fluxo WebViewPersistenceObject.** 
  
 _dwVersion_
  
> Deslocamento 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _dwType_
  
> Deslocamento 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).
    
 _dwFlags_
  
> Deslocamento 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _dwUnused[7]_
  
> Deslocamento 0xC, 28 bytes: todos os zeros.
    
 _cbData_
  
> Deslocamento 0x28, 4 bytes: 0x00000032.
    
 _wzURL_
  
> Deslocamento 0x2C, 0x32 bytes: matriz de 25 WCHARs. Um valor de cadeia de caracteres terminada em zero Unicode: " https://www.microsoft.com ".
    

