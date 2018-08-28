{
  "info": {
    "name": "Amazon EC2 Systems Manager API Modify Document Permission",
    "_postman_id": "386557da-804e-4f7a-91f9-b2c669dc2d66",
    "description": "Share a document publicly or privately.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Resources",
      "item": [
        {
          "id": "177eef58-8789-4aac-aa9f-b731c5c8f613",
          "name": "addTagsToResource",
          "request": {
            "url": "http://example.com/api/?Action=AddTagsToResource?ResourceId=ResourceId&ResourceType=ResourceType&Tags=Tags",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Adds or overwrites one or more tags for the specified resource."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "facce85b-1598-4b3e-8ed8-5bb1d15f77f7"
            }
          ]
        }
      ]
    },
    {
      "name": "Cancel",
      "item": [
        {
          "id": "b4e4a8f9-85aa-4f98-ab6d-f745f9ce8ee3",
          "name": "cancelCommand",
          "request": {
            "url": "http://example.com/api/?Action=CancelCommand?CommandId=CommandId&InstanceIds=InstanceIds",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Attempts to cancel the command specified by the Command ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "938d05b2-35ba-47bd-85c4-a9f76e430cad"
            }
          ]
        }
      ]
    },
    {
      "name": "Activation",
      "item": [
        {
          "id": "3e283a4e-64e2-4627-bc5c-bd52f626b209",
          "name": "createActivation",
          "request": {
            "url": "http://example.com/api/?Action=CreateActivation?DefaultInstanceName=DefaultInstanceName&Description=Description&ExpirationDate=ExpirationDate&IamRole=IamRole&RegistrationLimit=RegistrationLimit",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Registers your on-premises server or virtual machine with Amazon EC2 so that you can manage\n   these resources using Run Command."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "506c0532-144d-49e9-924c-70504e495631"
            }
          ]
        },
        {
          "id": "3fb80102-2d12-4a42-827b-1af393229b22",
          "name": "deleteActivation",
          "request": {
            "url": "http://example.com/api/?Action=DeleteActivation?ActivationId=ActivationId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes an activation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e82378cf-b70a-4c8a-8152-5e38f30f4748"
            }
          ]
        }
      ]
    },
    {
      "name": "Association",
      "item": [
        {
          "id": "ec4f4bd2-3cb9-46c6-a50d-8cdb9d90bab5",
          "name": "createAssociation",
          "request": {
            "url": "http://example.com/api/?Action=CreateAssociation?DocumentVersion=DocumentVersion&InstanceId=InstanceId&Name=Name&OutputLocation=OutputLocation&Parameters=Parameters&ScheduleExpression=ScheduleExpression&Targets=Targets",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Associates the specified SSM document with the specified instances or targets."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d053a184-c05f-44a2-835d-67f51e951800"
            }
          ]
        },
        {
          "id": "97f839e9-630b-4cfa-a28e-543aff83fb76",
          "name": "createAssociationBatch",
          "request": {
            "url": "http://example.com/api/?Action=CreateAssociationBatch?Entries=Entries",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Associates the specified SSM document with the specified instances or targets."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1ce9c313-dff9-49c7-94fd-ec6f64c1ab8b"
            }
          ]
        },
        {
          "id": "4a2a9223-5e20-4857-aeaf-251d55004c0d",
          "name": "deleteAssociation",
          "request": {
            "url": "http://example.com/api/?Action=DeleteAssociation?AssociationId=AssociationId&InstanceId=InstanceId&Name=Name",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Disassociates the specified SSM document from the specified instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f5fbb22f-2193-4498-8627-2155b413ac46"
            }
          ]
        },
        {
          "id": "f64d44e4-8a55-457b-a4a1-ef7aff8e7697",
          "name": "describeAssociation",
          "request": {
            "url": "http://example.com/api/?Action=DescribeAssociation?AssociationId=AssociationId&InstanceId=InstanceId&Name=Name",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes the associations for the specified SSM document or instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c0286cb7-a3ea-4da5-8b12-d8c8ba6c3a32"
            }
          ]
        }
      ]
    },
    {
      "name": "Document",
      "item": [
        {
          "id": "a6b69fe2-0e03-4d1e-aa74-fe3acaccbf88",
          "name": "createDocument",
          "request": {
            "url": "http://example.com/api/?Action=CreateDocument?Content=Content&DocumentType=DocumentType&Name=Name",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates an SSM document."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ef3a5f59-f642-438b-9d1d-5bb2c53530b0"
            }
          ]
        },
        {
          "id": "3af140fb-6b5f-4075-9c30-ec9f78e2cba3",
          "name": "deleteDocument",
          "request": {
            "url": "http://example.com/api/?Action=DeleteDocument?Name=Name",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the SSM document and all instance associations to the document."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "df9083ef-6cf1-4c81-bbf2-6d096bc5f64a"
            }
          ]
        },
        {
          "id": "ef155ab0-e54f-40a6-b084-bb0aa5ce17c0",
          "name": "describeDocument",
          "request": {
            "url": "http://example.com/api/?Action=DescribeDocument?DocumentVersion=DocumentVersion&Name=Name",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes the specified SSM document."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2f56a2c8-3b13-4a69-94fa-14e5ec611a39"
            }
          ]
        },
        {
          "id": "5332208c-2cf2-468c-afa6-e1668fabc0eb",
          "name": "describeDocumentPermission",
          "request": {
            "url": "http://example.com/api/?Action=DescribeDocumentPermission?Name=Name&PermissionType=PermissionType",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes the permissions for an SSM document."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d47dae78-f555-41f7-a925-3fda6fd718ce"
            }
          ]
        },
        {
          "id": "ab0026d4-2d7c-4549-86bc-60c8b0cb7ff4",
          "name": "getDocument",
          "request": {
            "url": "http://example.com/api/?Action=GetDocument?DocumentVersion=DocumentVersion&Name=Name",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the contents of the specified SSM document."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "29ac1dbf-64c9-40c7-8d97-17e7144cf4ab"
            }
          ]
        }
      ]
    },
    {
      "name": "Maintenance",
      "item": [
        {
          "id": "e3df3027-54f9-4441-81fc-9c47807c3cae",
          "name": "createMaintenanceWindow",
          "request": {
            "url": "http://example.com/api/?Action=CreateMaintenanceWindow?AllowUnassociatedTargets=AllowUnassociatedTargets&ClientToken=ClientToken&Cutoff=Cutoff&Duration=Duration&Name=Name&Schedule=Schedule",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new Maintenance Window."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b7e46ce7-1d3d-409d-8b1e-97698d59eaa1"
            }
          ]
        },
        {
          "id": "972dbf3e-a977-40c7-b117-e5d35beba848",
          "name": "deleteMaintenanceWindow",
          "request": {
            "url": "http://example.com/api/?Action=DeleteMaintenanceWindow?WindowId=WindowId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a Maintenance Window."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "de300c11-95b3-4b07-a01e-5e821113d472"
            }
          ]
        },
        {
          "id": "ab1635b2-3938-4ec4-bddc-17aa607156fe",
          "name": "describeMaintenanceWindowExecutions",
          "request": {
            "url": "http://example.com/api/?Action=DescribeMaintenanceWindowExecutions?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken&WindowId=WindowId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the executions of a Maintenance Window (meaning, information about when the\n   Maintenance Window was scheduled to be active and information about tasks registered and run with\n   the Maintenance Window)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9c25b2b1-9009-4e14-95b6-12308737a854"
            }
          ]
        },
        {
          "id": "86b2e061-1248-42cf-bb24-ab81f68ea633",
          "name": "describeMaintenanceWindowExecutionTaskInvocations",
          "request": {
            "url": "http://example.com/api/?Action=DescribeMaintenanceWindowExecutionTaskInvocations?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken&TaskId=TaskId&WindowExecutionId=WindowExecutionId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the individual task executions (one per target) for a particular task executed\n   as part of a Maintenance Window execution."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "09704cc6-9a3a-44e3-955b-f7d530addcf1"
            }
          ]
        },
        {
          "id": "88ac17da-2fdf-4c21-b23b-8c4ff5d5fa27",
          "name": "describeMaintenanceWindowExecutionTasks",
          "request": {
            "url": "http://example.com/api/?Action=DescribeMaintenanceWindowExecutionTasks?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken&WindowExecutionId=WindowExecutionId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "For a given Maintenance Window execution, lists the tasks that were executed."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6c6d5113-ca12-4895-af3c-1d3e04dc46ad"
            }
          ]
        },
        {
          "id": "396ab962-558b-426d-948a-22af128ee99b",
          "name": "describeMaintenanceWindows",
          "request": {
            "url": "http://example.com/api/?Action=DescribeMaintenanceWindows?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the Maintenance Windows in an AWS account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "79c7616d-5035-49c2-bd10-d1d6ced20de5"
            }
          ]
        },
        {
          "id": "e469dd51-d9e3-47ca-aaf7-30629de3368c",
          "name": "describeMaintenanceWindowTargets",
          "request": {
            "url": "http://example.com/api/?Action=DescribeMaintenanceWindowTargets?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken&WindowId=WindowId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the targets registered with the Maintenance Window."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "99c18ffa-f108-4965-9a88-9c0d7b3307e2"
            }
          ]
        },
        {
          "id": "9576dbfa-8f94-45a6-a8c3-d82291791b44",
          "name": "describeMaintenanceWindowTasks",
          "request": {
            "url": "http://example.com/api/?Action=DescribeMaintenanceWindowTasks?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken&WindowId=WindowId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the tasks in a Maintenance Window."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "db8d1a54-8963-45b9-85e5-beefea0555c3"
            }
          ]
        },
        {
          "id": "727b2878-5ab4-42d5-b0c6-bfe73d96c7a2",
          "name": "getMaintenanceWindow",
          "request": {
            "url": "http://example.com/api/?Action=GetMaintenanceWindow?WindowId=WindowId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves a Maintenance Window."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cf418c08-b242-4a78-a197-b38b8d1ddeb6"
            }
          ]
        },
        {
          "id": "17f31be8-7756-4b97-8436-4b134e844db2",
          "name": "getMaintenanceWindowExecution",
          "request": {
            "url": "http://example.com/api/?Action=GetMaintenanceWindowExecution?WindowExecutionId=WindowExecutionId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves details about a specific task executed as part of a Maintenance Window\n   execution."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "84d370b4-4017-4254-a4ad-32b43d8bf549"
            }
          ]
        },
        {
          "id": "1570cad2-3cfc-4ba8-9118-55de519f6888",
          "name": "getMaintenanceWindowExecutionTask",
          "request": {
            "url": "http://example.com/api/?Action=GetMaintenanceWindowExecutionTask?TaskId=TaskId&WindowExecutionId=WindowExecutionId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the details about a specific task executed as part of a Maintenance Window\n   execution."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "606301f0-5b2f-40a9-9c4f-cc566101ffe3"
            }
          ]
        }
      ]
    },
    {
      "name": "Baseline",
      "item": [
        {
          "id": "e5cafeaa-db63-4665-88d4-2582860f21f5",
          "name": "createPatchBaseline",
          "request": {
            "url": "http://example.com/api/?Action=CreatePatchBaseline?ApprovalRules=ApprovalRules&ApprovedPatches=ApprovedPatches&ClientToken=ClientToken&Description=Description&GlobalFilters=GlobalFilters&Name=Name&RejectedPatches=RejectedPatches",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a patch baseline."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "83f06c11-b036-45e8-b073-fccaabc3f281"
            }
          ]
        },
        {
          "id": "c943d1a3-98a0-4fa5-af9b-3b74a1957bf0",
          "name": "deletePatchBaseline",
          "request": {
            "url": "http://example.com/api/?Action=DeletePatchBaseline?BaselineId=BaselineId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a patch baseline."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ece6c5cc-796d-4912-8c03-233b704eb606"
            }
          ]
        },
        {
          "id": "c2c626d4-c220-4bce-9c9f-f441996c905a",
          "name": "getPatchBaseline",
          "request": {
            "url": "http://example.com/api/?Action=GetPatchBaseline?BaselineId=BaselineId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves information about a patch baseline."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "df4ea3db-0c26-4c87-afb9-1081c4309d2f"
            }
          ]
        }
      ]
    },
    {
      "name": "Parameter",
      "item": [
        {
          "id": "72b92ede-2d0a-42b6-a2c4-5906d0006c85",
          "name": "deleteParameter",
          "request": {
            "url": "http://example.com/api/?Action=DeleteParameter?Name=Name",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Delete a parameter from the system."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8b879564-31da-4f42-b127-a9f176a3aa74"
            }
          ]
        },
        {
          "id": "d24f0d2d-ee01-4522-a2ea-6095062c56b9",
          "name": "getParameterHistory",
          "request": {
            "url": "http://example.com/api/?Action=GetParameterHistory?MaxResults=MaxResults&Name=Name&NextToken=NextToken&WithDecryption=WithDecryption",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Query a list of all parameters used by the AWS account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e325a158-ca08-4b85-9ea7-0b19daf169ef"
            }
          ]
        }
      ]
    },
    {
      "name": "Deregister",
      "item": [
        {
          "id": "496c809a-0546-45a0-993f-92bb0db61a49",
          "name": "deregisterManagedInstance",
          "request": {
            "url": "http://example.com/api/?Action=DeregisterManagedInstance?InstanceId=InstanceId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Removes the server or virtual machine from the list of registered servers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6faa14a8-ce2b-40b8-8b8e-79cdb250a53c"
            }
          ]
        },
        {
          "id": "2d9328b1-0b3a-4ef1-854f-905b14f9a836",
          "name": "deregisterPatchBaselineForPatchGroup",
          "request": {
            "url": "http://example.com/api/?Action=DeregisterPatchBaselineForPatchGroup?BaselineId=BaselineId&PatchGroup=PatchGroup",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Removes a patch group from a patch baseline."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "28097a04-f3c5-4dad-b08a-f557fb0b2bb8"
            }
          ]
        },
        {
          "id": "3983e67c-f6b9-4f43-ba93-01393c9170e0",
          "name": "deregisterTargetFromMaintenanceWindow",
          "request": {
            "url": "http://example.com/api/?Action=DeregisterTargetFromMaintenanceWindow?WindowId=WindowId&WindowTargetId=WindowTargetId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Removes a target from a Maintenance Window."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3703bde3-bc88-4e05-be00-c95ff953b03d"
            }
          ]
        },
        {
          "id": "a81a6f02-d7cd-4f12-90a8-48233a87d7a8",
          "name": "deregisterTaskFromMaintenanceWindow",
          "request": {
            "url": "http://example.com/api/?Action=DeregisterTaskFromMaintenanceWindow?WindowId=WindowId&WindowTaskId=WindowTaskId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Removes a task from a Maintenance Window."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3e39fcd5-77a8-4019-9e69-33d6a25d2f06"
            }
          ]
        }
      ]
    },
    {
      "name": "Activations",
      "item": [
        {
          "id": "f2403106-66cd-461e-bd19-dd701b400e98",
          "name": "describeActivations",
          "request": {
            "url": "http://example.com/api/?Action=DescribeActivations?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Details about the activation, including: the date and time the activation was created,\n   the expiration date, the IAM role assigned to the instances in the activation, and the number of\n   instances activated by this registration."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e9077ec7-6515-4368-9f18-cf2219ec3ab4"
            }
          ]
        }
      ]
    },
    {
      "name": "Automation",
      "item": [
        {
          "id": "391c2a82-0a3a-42bd-beb5-faed4b956ca4",
          "name": "describeAutomationExecutions",
          "request": {
            "url": "http://example.com/api/?Action=DescribeAutomationExecutions?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Provides details about all active and terminated Automation executions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f509a469-5204-4fab-b44b-7a3f6536ae78"
            }
          ]
        },
        {
          "id": "947433da-6f0a-4ac0-95eb-a0480a389cfd",
          "name": "getAutomationExecution",
          "request": {
            "url": "http://example.com/api/?Action=GetAutomationExecution?AutomationExecutionId=AutomationExecutionId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get detailed information about a particular Automation execution."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cd9c9436-6d78-4337-91f5-f4ff0ac7b173"
            }
          ]
        }
      ]
    },
    {
      "name": "Available",
      "item": [
        {
          "id": "c67ef25c-77f5-4e9c-b099-3e0860da9ac6",
          "name": "describeAvailablePatches",
          "request": {
            "url": "http://example.com/api/?Action=DescribeAvailablePatches?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all patches that could possibly be included in a patch baseline."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "eecba8a7-21f9-421e-ac66-e19e68e1257e"
            }
          ]
        }
      ]
    },
    {
      "name": "Effective",
      "item": [
        {
          "id": "3b343ec5-f44f-4e62-91c0-ad7a989d41c2",
          "name": "describeEffectiveInstanceAssociations",
          "request": {
            "url": "http://example.com/api/?Action=DescribeEffectiveInstanceAssociations?InstanceId=InstanceId&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "All associations for the instance(s)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "18e270ae-aaf0-435c-a0da-8b7069e29a84"
            }
          ]
        },
        {
          "id": "14e5d5e8-0222-4cae-a41c-c4f1cc3749d9",
          "name": "describeEffectivePatchesForPatchBaseline",
          "request": {
            "url": "http://example.com/api/?Action=DescribeEffectivePatchesForPatchBaseline?BaselineId=BaselineId&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the current effective patches (the patch and the approval state) for the specified patch baseline."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec3902cb-d24e-468c-957c-f91609fdda80"
            }
          ]
        }
      ]
    },
    {
      "name": "Instance",
      "item": [
        {
          "id": "d7bf70a7-6f46-446a-a759-5a0902e47a72",
          "name": "describeInstanceAssociationsStatus",
          "request": {
            "url": "http://example.com/api/?Action=DescribeInstanceAssociationsStatus?InstanceId=InstanceId&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The status of the associations for the instance(s)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "775fb6a0-cf8c-4fdb-a279-050f126ab589"
            }
          ]
        },
        {
          "id": "6636821c-b96d-4f32-8436-f334a5ab19e2",
          "name": "describeInstanceInformation",
          "request": {
            "url": "http://example.com/api/?Action=DescribeInstanceInformation?Filters=Filters&InstanceInformationFilterList=InstanceInformationFilterList&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes one or more of your instances."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4533c877-4c11-4f23-b40f-be203f116593"
            }
          ]
        },
        {
          "id": "f4871b0f-8dba-4385-94c6-3a540306976d",
          "name": "describeInstancePatches",
          "request": {
            "url": "http://example.com/api/?Action=DescribeInstancePatches?Filters=Filters&InstanceId=InstanceId&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves information about the patches on the specified instance and their state relative to the patch baseline being used for the instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "08b313dd-7a63-4249-b36b-99c03e04fb99"
            }
          ]
        },
        {
          "id": "45aff1d7-cfc9-4e85-8edf-59f2a7c8d77f",
          "name": "describeInstancePatchStates",
          "request": {
            "url": "http://example.com/api/?Action=DescribeInstancePatchStates?InstanceIds=InstanceIds&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the high-level patch state of one or more instances."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "caf0da77-c5d1-4508-b477-e9ce3f7784ff"
            }
          ]
        },
        {
          "id": "92c27cd8-5f44-4e15-82e0-b09bca708191",
          "name": "describeInstancePatchStatesForPatchGroup",
          "request": {
            "url": "http://example.com/api/?Action=DescribeInstancePatchStatesForPatchGroup?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken&PatchGroup=PatchGroup",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the high-level patch state for the instances in the specified patch group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "53afe9bd-9252-4d0b-ba6f-068d2361c21d"
            }
          ]
        }
      ]
    },
    {
      "name": "Parameters",
      "item": [
        {
          "id": "92656faf-926e-477f-aa2f-f2aec06744d8",
          "name": "describeParameters",
          "request": {
            "url": "http://example.com/api/?Action=DescribeParameters?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get information about a parameter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b9d839b8-86ae-4c41-99b5-1f466aea2587"
            }
          ]
        },
        {
          "id": "1bef70e5-ad58-4a63-8159-4561bafb129d",
          "name": "getParameters",
          "request": {
            "url": "http://example.com/api/?Action=GetParameters?Names=Names&WithDecryption=WithDecryption",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a list of parameters used by the AWS account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "22968398-3ab0-4cc6-855a-66e908dfd426"
            }
          ]
        }
      ]
    },
    {
      "name": "Baselines",
      "item": [
        {
          "id": "c4f7e9be-aae7-4b0e-9a27-943edc6146ed",
          "name": "describePatchBaselines",
          "request": {
            "url": "http://example.com/api/?Action=DescribePatchBaselines?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the patch baselines in your AWS account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7289f992-e068-4b94-aed7-ce7f83e9ed2a"
            }
          ]
        }
      ]
    },
    {
      "name": "Groups",
      "item": [
        {
          "id": "70910981-d86e-4046-bd0d-0462a0cd35f4",
          "name": "describePatchGroups",
          "request": {
            "url": "http://example.com/api/?Action=DescribePatchGroups?MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all patch groups that have been registered with patch baselines."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ed783b91-1a14-4259-8de1-3fb29b77e2cf"
            }
          ]
        }
      ]
    },
    {
      "name": "Group",
      "item": [
        {
          "id": "c7967174-55f5-4ec3-b3d2-c5387fcedde5",
          "name": "describePatchGroupState",
          "request": {
            "url": "http://example.com/api/?Action=DescribePatchGroupState?PatchGroup=PatchGroup",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns high-level aggregated patch compliance state for a patch group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0f6910ff-663d-4b07-ae2b-e86a68e23702"
            }
          ]
        }
      ]
    },
    {
      "name": "Command",
      "item": [
        {
          "id": "2330c115-2d0c-4907-9182-bf19479e716e",
          "name": "getCommandInvocation",
          "request": {
            "url": "http://example.com/api/?Action=GetCommandInvocation?CommandId=CommandId&InstanceId=InstanceId&PluginName=PluginName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns detailed information about command execution for an invocation or plugin."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d9242431-38a1-4074-a4a6-b266825556b1"
            }
          ]
        }
      ]
    },
    {
      "name": "Default",
      "item": [
        {
          "id": "079ddfc1-8ec4-4d42-9914-7d588e72c416",
          "name": "getDefaultPatchBaseline",
          "request": {
            "url": "http://example.com/api/?Action=GetDefaultPatchBaseline?BaselineId=BaselineId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the default patch baseline."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "08954265-6dc7-47a4-9700-39ef857ef2d8"
            }
          ]
        }
      ]
    },
    {
      "name": "Deployable",
      "item": [
        {
          "id": "b6f8b76f-2800-4ec5-8573-40d7fbc72915",
          "name": "getDeployablePatchSnapshotForInstance",
          "request": {
            "url": "http://example.com/api/?Action=GetDeployablePatchSnapshotForInstance?InstanceId=InstanceId&SnapshotId=SnapshotId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the current snapshot for the patch baseline the instance uses."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8b3457f8-009b-4388-bb16-f30d7e59afe9"
            }
          ]
        }
      ]
    },
    {
      "name": "Inventory",
      "item": [
        {
          "id": "eafed358-4fd3-4c77-9d5d-66861cfc5d08",
          "name": "getInventory",
          "request": {
            "url": "http://example.com/api/?Action=GetInventory?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken&ResultAttributes=ResultAttributes",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Query inventory information."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "51b9d47b-0987-4c58-b249-aed701f2bf1d"
            }
          ]
        },
        {
          "id": "932c4b63-1f5f-4dcf-ae59-632a9bd3e8c3",
          "name": "getInventorySchema",
          "request": {
            "url": "http://example.com/api/?Action=GetInventorySchema?MaxResults=MaxResults&NextToken=NextToken&TypeName=TypeName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Return a list of inventory type names for the account, or return a list of attribute\n   names for a specific Inventory item type."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0b0f9195-1803-4268-9a1c-712cd6b7a38d"
            }
          ]
        }
      ]
    },
    {
      "name": "BaselineGroup",
      "item": [
        {
          "id": "e23f4545-2b0d-47ac-a501-a0d66adb43c3",
          "name": "getPatchBaselineForPatchGroup",
          "request": {
            "url": "http://example.com/api/?Action=GetPatchBaselineForPatchGroup?PatchGroup=PatchGroup",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the patch baseline that should be used for the specified patch group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f3bfb4db-5da6-4f3e-b40f-9eaf38d454a2"
            }
          ]
        }
      ]
    },
    {
      "name": "List",
      "item": [
        {
          "id": "fa9aed3e-0767-45af-8f46-2b53d22b3946",
          "name": "listAssociations",
          "request": {
            "url": "http://example.com/api/?Action=ListAssociations?AssociationFilterList=AssociationFilterList&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the associations for the specified SSM document or instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0c9248ac-c8a2-4b1b-a551-8acec368179f"
            }
          ]
        },
        {
          "id": "58a97652-e24c-4513-96d5-fc6862fb83aa",
          "name": "listCommandInvocations",
          "request": {
            "url": "http://example.com/api/?Action=ListCommandInvocations?CommandId=CommandId&Details=Details&Filters=Filters&InstanceId=InstanceId&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "An invocation is copy of a command sent to a specific instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "148add39-2665-4069-b7f7-d6acd4f27f9a"
            }
          ]
        },
        {
          "id": "d27b70b5-fa4b-4458-9e33-3f04e36d97b6",
          "name": "listCommands",
          "request": {
            "url": "http://example.com/api/?Action=ListCommands?CommandId=CommandId&Filters=Filters&InstanceId=InstanceId&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the commands requested by users of the AWS account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e80b372c-a941-433b-a538-621ce69d1530"
            }
          ]
        },
        {
          "id": "bca65183-819f-4a8c-9ce9-b661b749514a",
          "name": "listDocuments",
          "request": {
            "url": "http://example.com/api/?Action=ListDocuments?DocumentFilterList=DocumentFilterList&MaxResults=MaxResults&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes one or more of your SSM documents."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4c2c1249-80e7-4e44-a1ba-5c2914e1858c"
            }
          ]
        },
        {
          "id": "4aab0f61-5869-49f2-81a1-e1df5fa5eb5c",
          "name": "listDocumentVersions",
          "request": {
            "url": "http://example.com/api/?Action=ListDocumentVersions?MaxResults=MaxResults&Name=Name&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all versions for a document."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "34735807-9b5a-4f36-bdc3-675da14a0ba8"
            }
          ]
        },
        {
          "id": "6af6e673-52f7-4498-8943-a4296b1e0f04",
          "name": "listInventoryEntries",
          "request": {
            "url": "http://example.com/api/?Action=ListInventoryEntries?Filters=Filters&InstanceId=InstanceId&MaxResults=MaxResults&NextToken=NextToken&TypeName=TypeName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "A list of inventory items returned by the request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "07cac8c3-dabb-4560-bb8f-50b8e314ef9c"
            }
          ]
        },
        {
          "id": "8af33f07-52be-4cf4-9c61-612412eb7d51",
          "name": "listTagsForResource",
          "request": {
            "url": "http://example.com/api/?Action=ListTagsForResource?ResourceId=ResourceId&ResourceType=ResourceType",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of the tags assigned to the specified resource."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a140671b-f7fa-4c4a-9377-44ed812abf72"
            }
          ]
        }
      ]
    },
    {
      "name": "Modify",
      "item": [
        {
          "id": "c9e0c15b-ee94-4e7f-81f5-5a382bc5b94e",
          "name": "modifyDocumentPermission",
          "request": {
            "url": "http://example.com/api/?Action=ModifyDocumentPermission?AccountIdsToAdd=AccountIdsToAdd&AccountIdsToRemove=AccountIdsToRemove&Name=Name&PermissionType=PermissionType",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Share a document publicly or privately."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "72a94161-aa49-44d3-9e2b-9f6e1013ffad"
            }
          ]
        }
      ]
    }
  ]
}