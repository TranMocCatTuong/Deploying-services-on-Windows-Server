# How to Create Your Group Policy Object?

1. Open Server Manager, [1] select Tools, [2] choose **Group Policy Management**.

  ![ Image 1. ](/img/5_1.png)

2. Select **Domain**.

  ![ Image 2. ](/img/5_2.png)

3. Select your domain.

![ Image 3. ](/img/5_3.png)

4. Select **Group Policy Objects**.

![ Image 4. ](/img/5_4.png)

5. Right-click in the empty space, then select **New**.

![ Image 5. ](/img/5_5.png)

6. [1] Enter the name for the GPO, then [2] click **OK**.

![ Image 6. ](/img/5_6.png)

7. Right-click on the newly created GPO, then click **Edit**.

![ Image 7. ](/img/5_7.png)

8. Select **Computer Configuration**.

![ Image 8. ](/img/5_8.png)

9. Select **Policies**.

![ Image 9. ](/img/5_9.png)

10. Select **Windows Settings**.

![ Image 10. ](/img/5_10.png)

11. Select **Security Settings**.

![ Image 11. ](/img/5_11.png)

12. Select **File System**.

![ Image 12. ](/img/5_12.png)

13. Right-click in the empty space, then select ***Add File...***.

![ Image 13. ](/img/5_13.png)

14. [1] Select the folder you want to configure security for, then [2] click **OK**.

![ Image 14. ](/img/5_14.png)

15. Remove default groups and users.

![ Image 15. ](/img/5_15.png)

16. Select **Add...**.

![ Image 16. ](/img/5_16.png)

17. Enter the object names to select, then click **OK**.

![ Image 17. ](/img/5_17.png)

18. [1] Configure **Full Control** permissions according to the [**User Permissions by Department**](https://github.com/TranMocCatTuong/Deploying-services-on-Windows-Server?tab=readme-ov-file#user-permissions-by-department)  table. [2] Then click **OK** to finish.

![ Image 18. ](/img/5_18.png)

