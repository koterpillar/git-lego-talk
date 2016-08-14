# Me

Alexey Kotlyarov
@koterpillar
Common Code

# Git as Lego

* What did the merge do?
* Someone rebased, help me now
* How do I get FunkyBob/Linus to not swear at my PR

# Changes

README.md
manage.py
blog/
    models.py
    views.py

# Changes

     /---------- README.md
     |   /------ manage.py
     |   |   /-- blog/models.py
     |   |   |
    +-+ +-+ +-+
  +-+ +-+ +-+ +--+
  |              |
  +--------------+

# More changes

     /-------------- README.md
     |   /---------- manage.py
     |   |   /------ blog/models.py
     |   |   |   /-- blog/views.py
    +-+ +-+ +-+ +-+
  +-+ +-+ +-+ +-+ +--+
  |                  |
  | +-+ +-+ +-+      |
  +-+ +-+ +-+ +------+

    +-+ +-+ +-+
  +-+ +-+ +-+ +--+
  |    parent    |
  +--------------+

# More changes

      master
    +-+ +-+ +-+
  +-+ +-+ +-+ +--+
  |              |
  | +-+ +-+ +-+  |
  +-+ +-+ +-+ +--+
  |              |
  | +-+ +-+ +-+  |
  +-+ +-+ +-+ +--+
  |              |
  +--------------+

# Branches

  feature
   +-+
  ++ +-+
  |    |    master
  |+-+ |    +-+
  \+ +-\  /-+ +-/
   \    \/     /
    \   /     /
     \ /     /
      +-+ +-+
      |     |
      +-----+

# Merges

         +------+
        / \      \
       / /=\      \====== fits feature
      /  *  \  *========= fits master
     /+-+  / \  +-+ \
     ++ +-+   +-+ +-+


  feature
   +-+
  ++ +-+
  |    |    master
  |+-+ |    +-+
  \+ +-\  /-+ +-/
   \    \/     /
    \   /     /
     \ /     /
      +-+ +-+
      |     |
      +-----+

# Rebases

        feature
         +-+
        ++ +-+
        |    |
        |+-+ |
        \+ +-\ 
         \    \ 
          \    \ 
           \  +-\  <===== this will not fit!
            +-+ ++


            master
            +-+
          /-+ +-/
         /     /
        /     /
       /     /
      +-+ +-+
      |     |
      +-----+

# Rebases

        feature
         +-+
        ++ +-+
        |    |
        |+-+ |   <===== and now this doesn't fit!
        \+ +-\ 

         +-+
       \-+ +--\ 
        \      \ 
         \      \ 
          \ +-+  +
          /-+ +-/
         /     /
        /     /
       /     /
      +-+ +-+
      |     |
      +-----+

# Rebase -i

         +-+
        \+ +-\ 
         \    \ 
          \    \ 
           \  +-\
            +-+ ++

         +-+
        ++ +-+
        |    |
        |+-+ |

            master
            +-+
          /-+ +-/
         /     /
        /     /
       /     /
      +-+ +-+
      |     |
      +-----+

# Squash

    +-+ +-+ +-+           +-+ +-+ +-+
  +-+ +-+ +-+ +--+      +-+ +-+ +-+ +--+
  |              |      |              |
  | +-+ +-+ +-+  |      |              |
  +-+ +-+ +-+ +--+      |              |
  |              |  =>  |              |
  | +-+ +-+ +-+  |      |              |
  +-+ +-+ +-+ +--+      |              |
  |              |      |              |
  +--------------+      +--------------+
