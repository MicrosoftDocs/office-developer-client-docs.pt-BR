---
title: Função OPENFILE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Abre um documento do Microsoft Visio, se ainda não estiver aberto, e ativa a janela de documento.
ms.openlocfilehash: 5a89a658e560d144007ec19796de82b9949bea82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419573"
---
# <a name="openfile-function"></a>Função OPENFILE

Abre um documento do Microsoft Visio, se ainda não estiver aberto, e ativa a janela de documento.
  
## <a name="syntax"></a>Sintaxe

 **OPENFILE**( _"filename"_)
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _filename_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome do arquivo, incluindo o caminho do arquivo, que você deseja abrir.  <br/> |
   
## <a name="remarks"></a>Comentários

Chamadas múltiplas da função OPENFILE permanecem na fila e são executadas por ordem de avaliação. Se o documento atual do Visio estiver ativo para edição visual (in-loco), uma nova instância do Visio será inicializada com o nome de arquivo solicitado. 
  
Essa função sempre retornará FALSO. 
  
Em versões anteriores do aplicativo Visio, essa função aparece como _OPENFILE. As versões 4.0 e posteriores do Visio aceitam os dois estilos. 
  
## <a name="example"></a>Exemplo

 `OPENFILE("C:/MyFile.vsdx")`
  
Abre o arquivo especificado "MyFile.vsdx" em uma nova janela ou ativa a janela se o arquivo já estiver aberto. 
  

