# Answers

You need to create two different commits. One to each feature.

## Commit 1
```
add teams endpoint

We want to get teams related to a user.
```
```
--- a/openapi.json
+++ b/openapi.json
@@ -45,6 +45,7 @@
           }
         }
       }
-    }
+    },
+    "/user/{userId}/teams": {
        ...
      }
   }
 }
```

```
+++ b/openapi.test.txt
@@ -1,2 +1,3 @@
 Testing path:
- - "/user/{userId}"
\ No newline at end of file
+ - "/user/{userId}"
+ - "/user/{userId}/teams"
```
## Commit 2

```
add organization endpoint

We want to get organizations related to a user.
```
```
--- a/openapi.json
+++ b/openapi.json
@@ -45,6 +45,7 @@
           }
         }
       }
-    }
+    },
+    "/user/{userId}/organizations": {
        ...
      }
   }
 }
```

```
+++ b/openapi.test.txt
@@ -1,2 +1,3 @@
 Testing path:
- - "/user/{userId}"
- - "/user/{userId}/teams"
\ No newline at end of file
+ - "/user/{userId}"
+ - "/user/{userId}/teams"
+ - "/user/{userId}/organizations"
```